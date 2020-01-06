# Craft — hackthebox

This is a write-up on how I solved craft from HacktheBox.

![](img/1__hkyydqOLVEybt__rUpz3S4w.png)

This is a write-up on how I solved craft from HacktheBox.

[Hack the Box](http://hackthebox.eu/) is an online platform to test and advance your skills in penetration testing and cybersecurity.

### About this box:

One of my favorite boxes from HackTheBox, very real-world applicable. There are lots of steps, but it’s very straightforward and you probably have already found your next step before you know how to use it, we will see a lot of common mistakes, this one really forces you to understand all the pieces of the web-app it is running in order to get user. So it feels very real.

Actually, Craft was my first Medium level box.

### Recon:

Use Nmap to scan the target ports:

![](img/1__E__jspoUOY6Qjo6dHZcUSGg.png)

> **nmap** Network exploration tool and security / port scanner  
> **\-sV** (Version detection)   
> **\-sC** Performs a script scan using the default set of scripts.

Only two ports are opened 22 and 443. We can directly access to [https://10.10.10.110](https://10.10.10.110) and see what we get.

![](img/1__FcctlriPFrdSfZebLMmSKg.png)

So, we got a simple page, if we navigate to the source we get two URL.

https://api.craft.htb/api/  
https://gogs.craft.htb/

![](img/1__LhX__gzFJRjPUrvTMzAV3Xg.png)

To access these URLs we need to add them in the host file.

Open hosts file with your favorite editor and add the IP address and URLs:

sudo vim /etc/hosts

![](img/1__4W2BrGIzQBGOqBJtPjid8Q.png)

We have craft API:

![](img/1__412bo93DszQhZLPOxin44Q.png)

And also we have “A painless self-hosted Git service.” — [GOGS](https://gogs.io), where craft-API source code is hosted:

![](img/1__rBCr2Z7KLsWZIXTUYL8wDw.png)

And we got a flask based web application:

![](img/1__IyCTfAPcROe23vC4jrf59A.png)

### Let’s dive into code

If we look at API modules, we will see ‘eval’ function in

craft\_api/api/brew/endpoints/brew.py

![](img/1__FMgu3zS__YZ__2DFwUmaIYUQ.png)

Eval is a very dangerous function, we can use it to [execute System command](http://vipulchaskar.blogspot.com/2012/10/exploiting-eval-function-in-python.html).

However, when a user is able to provide the input, `eval()` will execute anything that’s fed to it. A user could build a string where additional python code is executed, such as erasing all files on the system or spawning a reverse shell. Therefore, `eval()` should never be used to process user input.

We see that `eval()` is used to make sure the ‘abv’ value submitted by the user is less than 1.0.

It expects something like this:

![](img/1__lHPGt3dKAd__Zy3pHzfs2PA.png)

We can exploit this by sending the following POST request to the API, which would open a reverse shell to the device with IP 10.10.15.130 on Port 9999.

![](img/1__DopAYt2rL9te4TOZha4PEA.png)

BUT, this won’t spawn the reverse shell, To trigger the eval function, we need to send an authorized request on brew endpoint.

### Get reverse shell

For authorization, we need the username and password. Random/Default one does not work. Let's continue looking at the Gogs repository.

![](img/1__mwBl__Lo5P3MmUPYX1uBb7g.png)

If we look at the commit history, we will see that Dinesh has no idea about cyber hygiene. he left username and password in the history:

![](img/1__Nres3klQy2Jsrp1tIy837w.png)

Let’s generate token and send an authorized request on the API:

![[https://gist.github.com/ls4cfk/ab6c1115f3f3da247b65041e93771486#file-exploit-py](https://gist.github.com/ls4cfk/ab6c1115f3f3da247b65041e93771486#file-exploit-py)](img/1__cSWQfXQ8fnP__IeIyAG4AbA.png)
[https://gist.github.com/ls4cfk/ab6c1115f3f3da247b65041e93771486#file-exploit-py](https://gist.github.com/ls4cfk/ab6c1115f3f3da247b65041e93771486#file-exploit-py)

First set up a listener on port 9999:

nc -nvlp 9999

![](img/1__KMx__MSim40__vPUC1seB4Mg.png)

And run our python script:

![](img/1__loU8lFKf__CGJhWPg1mJ3PQ.png)

We got the shell!

Wait a sec! we are root? Where is the flag?

![](img/1__X9CnwxFuK6DA__M3GbAuO__Q.png)

We are in jail! It’s a docker container.

![](img/1__TnB8FxJ2fBZaFCAIcAuUCA.png)

Okay, let's look at what we got.

We have the same repository but the difference is that we got credentials of the MySQL

![](img/1__aWtFiFyADeaE9T1KCX7uaQ.png)

From `database/models.py` we know that there is 2 table in our database.

![](img/1__AzAbQynb3A6USXsUYJ__4Zg.png)

We can modify `dbtest.py` code and dump all the content from the “user” table

![](img/1__Un____E80BmRuts1LK3N0GIw.png)

Change SQL query to:

sql = "SELECT \* FROM \`user\`"

And to get all row:

result = cursor.fetchone()   
 **=>**result = cursor.fetchall()

We get new credentials!

![](img/1__WfQEpeMx__nX7oMQcjA9mrw.png)

Use those credentials to log in on Gogs, Ebachman’s credentials do not work but we can log in as a Gilfoyle.

![](img/1__4Klj1o54STmK1u6f9y6ZhA.png)

Oh man, Gilfoyle has a secret repository that contains a .ssh folder. Why him? he is my idol! c’mon… it should be Denish 🤣

![](img/1__lofhUd5kFc6wOXxfjfOzYg.png)

We have a public and private key:

![](img/1__JwprPCamCvs46E65d56yRA.png)

Okay, grab id\_rsa and ssh via Gilfoyle’s account:

ssh -i id\_rsa gilfoyle@10.10.10.110

![](img/1__QoTDsEEyahUTHMTHTwxHsQ.png)

Oh crap, it needs the passphrase. I tried to crack it with John but it took me a while and realized that it can be the password of Gilfoyle’s account.

> Use ‘ZEU3N8WNM2rh4T’ as passphrase and we are in!

![](img/1__toQLazmPkh6ipfIw5wcnCw.png)

Okay, we can read user.txt and submit it for 15 points:

![](img/1__OMTjZx9WoS39HIUTbcvLnA.png)

### Privilege escalation

From the secret repository, we know that we have vault on our box

![](img/1____5O8l8fWZ0t7Pnny__tEXIg.png)

> **Vault** is a tool for securely accessing secrets. A secret is anything that you want to tightly control access to, such as API keys, passwords, SSH keys, or certificates. **Vault** provides a unified interface to any secret while providing tight access control and recording a detailed audit log.

> — [https://www.vaultproject.io](https://www.vaultproject.io/docs/what-is-vault/index.html)

In the vault directory, we also have secrets.sh file

![](img/1__YM__UhT2aO8roW5TezmodtA.png)

It appears as though he’s running vault as root.

![](img/1__CLuk4GxO__otACGLYBuijdA.png)

With the following command, we can generate OTP(one-time password) for SSH.

```
vault write ssh/creds/root_otp ip=10.10.10.110
```

And we are root!

![](img/1__K9DN__IbEvFWlBKDn__XAm8Q.png)

It was my first writeup about HackThebox, I hope you enjoyed!

Feedback is welcome.

<script src="https://www.hackthebox.eu/badge/94787"></script>
### References

1\. http://vipulchaskar.blogspot.com/2012/10/exploiting-eval-function-in-python.html  
2\. http://pentestmonkey.net/cheat-sheet/shells/reverse-shell-cheat-sheet/  
3\. [https://www.vaultproject.io/docs/commands/ssh.html](https://www.vaultproject.io/docs/commands/ssh.html)

4\. [https://carbon.now.sh/](https://carbon.now.sh/)

By [Aleksi Kistauri](https://medium.com/@aleksikistauri) on [January 4, 2020](https://medium.com/p/fd1dd7842586).

[Canonical link](https://medium.com/@aleksikistauri/craft-hackthebox-fd1dd7842586)

Exported from [Medium](https://medium.com) on January 6, 2020.
