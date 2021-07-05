## TOMCAT WALKTHROUGH

İlk olarak makineyi çalıştırıyoruz.


![tomcat](https://user-images.githubusercontent.com/55113204/124516175-c52b4d80-dde9-11eb-9030-901aed69af3e.PNG)


Çalıştırılan makinenin ip adresini öğrenmek için netdiscover aracını kullanıyoruz.

![tomcat0](https://user-images.githubusercontent.com/55113204/124516213-d4120000-dde9-11eb-9897-fe9cc247ec91.PNG)


![tomcat1](https://user-images.githubusercontent.com/55113204/124516236-de33fe80-dde9-11eb-85b6-5100f4ec1214.PNG)


IP adresi öğrenilen makinenin açık olan servislerini ve port taramalarını gerçekleştiriyoruz. 

![tomcat2](https://user-images.githubusercontent.com/55113204/124516289-f86ddc80-dde9-11eb-9c26-01b6caa7451e.PNG)

Buradan elde edilen bilgilere göre port 22 üzerinde bulunan SSH servisi ile port 8080 üzerinde bulunan HTTP servisi açık olduğu görülmektedir. İlk olarak yapmamız gerek işlem açık olan HTTP portunu tarayıcıdan kontrol etmektir.

![tomcat3](https://user-images.githubusercontent.com/55113204/124516522-82b64080-ddea-11eb-8556-de03cbad9683.PNG)

Görüldüğü gibi karşımıza 8080 HTTP servisinde çalışan siteleri çıktı. Siteyi incelediğimizde gözüme Manager App alanı çıkıyor. Hadi burayı Metasploitle kurcalayalım.

![tomcat4](https://user-images.githubusercontent.com/55113204/124516708-f5272080-ddea-11eb-88ff-6863a8b57750.PNG)

Şimdi exploit kullanarak login olalım.

![tomcat5](https://user-images.githubusercontent.com/55113204/124516932-7979a380-ddeb-11eb-875e-8af296a06412.PNG)

Bingo !! Bulduk.

![tomcat6](https://user-images.githubusercontent.com/55113204/124517058-aded5f80-ddeb-11eb-832d-559ab3a74807.PNG)

Ve bakalım içerde miyizz ?? Yeap :)

![tomcat7](https://user-images.githubusercontent.com/55113204/124517148-eb51ed00-ddeb-11eb-957d-39d46d2bf92d.PNG)

![tomcat8](https://user-images.githubusercontent.com/55113204/124517154-f147ce00-ddeb-11eb-9e70-01c5311e70f7.PNG)

Reverse bağlantı serverdan dışarıya olan bağlantıdır. Bind bağlantı ise clientten servera doğru olan bağlantıdır. Şimdi shell alalım. Bunun için kendi Localhostumuzu ve dinlenecek Portu bilgileri ile reverse shell ile sunucudan dışarıya dinleme yapalım. Ve bir shell dosyası oluşturup içine atalım.

![tomcat9](https://user-images.githubusercontent.com/55113204/124518185-7cc25e80-ddee-11eb-8d2a-642bdb8a8841.PNG)

Reverse bağlantıyı bize 7777 portundan verecek. War dosyasını serverda çalıştırdığımızda bize reverse bir bağlantı sunucak. Dosyayı yükledikten sonra Netcat ile dinleme yapalım. Burada l (listen) v (verbose olarak) n (dns i çöz) p (port 777) olarak dinleme yapıyoruz. Ve makinenin içinde miyiz diye yükledikten sonra kontrol ediyoruz.

![tomcat10](https://user-images.githubusercontent.com/55113204/124518795-19d1c700-ddf0-11eb-8328-6c555818e070.PNG)

![tomcat11](https://user-images.githubusercontent.com/55113204/124518802-1d654e00-ddf0-11eb-991d-9237c6a83c1d.PNG)

![tomcat12](https://user-images.githubusercontent.com/55113204/124518806-21916b80-ddf0-11eb-9b9a-8de8dbc2716c.PNG)

![tomcat13](https://user-images.githubusercontent.com/55113204/124518858-48e83880-ddf0-11eb-97d0-0396db1e3048.PNG)

![tomcat14](https://user-images.githubusercontent.com/55113204/124518966-9d8bb380-ddf0-11eb-9fdd-32592fd21205.PNG)


Python ile bash shelli alalım.

![tomcat15](https://user-images.githubusercontent.com/55113204/124519120-125eed80-ddf1-11eb-9394-56b42887f83e.PNG)

Hadi root olmak için önce yetkilerimize bakalım. Burada bir javayı root yetkisinde çalıştırabileceğimiz anlamına gelmektedir. Bundan dolayı makineye bir java dosyası atılmalı ki ondan reverse shell alınsın. Bir meterpreter payloadı kullanalım. 

![tomcat16](https://user-images.githubusercontent.com/55113204/124520009-c9f4ff00-ddf3-11eb-8310-a1aa3d2491ac.PNG)

![tomcat17](https://user-images.githubusercontent.com/55113204/124519987-b77ac580-ddf3-11eb-8d29-08dfccda0d05.PNG)

Şimdi bunu karşı makineye atalım. Önce karşı makinede yazma izni olan bir dosya bulmalıyız. Bu dosyaları aşağıdaki komut ile bulabiliriz.

![tomcat18](https://user-images.githubusercontent.com/55113204/124520179-52739f80-ddf4-11eb-8e2f-a0791fa7832e.PNG)

Burada temp dosyasına yazma iznimiz olduğunu öğrendik. 

![tomcat19](https://user-images.githubusercontent.com/55113204/124520283-9cf51c00-ddf4-11eb-808b-cc5f95dbd6f7.PNG)

Şimdi rsm.jar dosyamızı hedef makineye atalım. Hedef makineye dosya göndermenin birçok yöntemi var. HTTP Server, FTP, SMB, Netcat, Powershell (windows için) aracılıkları ile dosya gönderebilmekteyiz. HTTP Server var mı kontrol edelim. Ve dizinlerimizde wget var mı yok mu kontrol edelim.
Yeap wgete sahibiz.

![tomcat20](https://user-images.githubusercontent.com/55113204/124520599-9024f800-ddf5-11eb-9229-50c522685968.PNG)

Apache HTTP Serverı açalım. Ve tüm dosyalarımızı sunalım.

![tomcat21](https://user-images.githubusercontent.com/55113204/124520778-2527f100-ddf6-11eb-99c5-84d82e260254.PNG)


Ve wget ile kendi makinemizdeki jar dosyasını hedef makineye çekelim. 
Burada sırasıyla wget -o komutu ile birden fazla dosya çekebilmekteyiz. Çektiğimiz dosyayı hangi isimle oluşturacaksak onu yazarız. Hangi makineden ise onun http://ip/çekilecek_dosya olarak yazarız. Ve hangi dosyayı çekeceksek onu ekleriz.

![tomcat22](https://user-images.githubusercontent.com/55113204/124521113-1beb5400-ddf7-11eb-9b79-0121b524a3f8.PNG)

Metasploitten dinlemeye geçelim. Multi/handler exploiti ile dinleme yapabiliriz. Kendi makinemizde payloadımızı nasıl yazmış isek hedef metasploittede öyle yazmamız gerekiyor. Port ve Localhostlarımızı da yazdıktan sonra dinlemeye geçmeliyiz. Bu şekilde verdiğimiz dosya aracılığı ile hedef makinede yetki yükseltebiliriz.

![image](https://user-images.githubusercontent.com/55113204/124521585-b5673580-ddf8-11eb-94c1-a9537416b585.png)

Bana shelli açması için yüklediğimiz jar dosyasını açıyorum ve meterpreter tarafından açıldığına dair bilgi alıyorum.

![tomcat24](https://user-images.githubusercontent.com/55113204/124521857-b51b6a00-ddf9-11eb-87ba-ee6aca951111.PNG)

![tomcat25](https://user-images.githubusercontent.com/55113204/124521893-d419fc00-ddf9-11eb-90f5-6485bc48e0f5.PNG)

Ve root olduğumuzu meterpreter ile öğrenelim bakalım.

![tomcat26](https://user-images.githubusercontent.com/55113204/124521942-0cb9d580-ddfa-11eb-80b5-9c988cfd23aa.PNG)

Yeap artık tam yetki bizde çünkü biz rootuz artık. 

Bir sonraki makine çözümünde görüşmek üzere :)


**¯\\\_(ツ)\_/¯**








