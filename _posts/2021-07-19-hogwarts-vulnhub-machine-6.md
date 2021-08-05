## HOGWARTS

Merhaba bugün hogwarts makine çözümü ile karşınızdayım. İlk önce makineyi vm kurup çalıştırıyorum. Daha sonra ilk yaptığım şey netdiscover aracını kullanarak makinenin ip adresini
öğrenmek. Hadi başlayalım o zaman :)

![hogwarts](https://user-images.githubusercontent.com/55113204/126190277-e4d28c58-26b2-4ab6-97f1-43c23f839176.png)

Evet ip adresini almış olduk. Şimdi nmap aracını kullanarak ağ haritalanmasına bakalım. Hangi portları açık yada değil onu öğrenelim.

![hogwarts1](https://user-images.githubusercontent.com/55113204/126190628-1be645fb-6105-44c2-bec7-803a3123f465.png)

Yeap 80 portu açıkmış. Hadi bir kontrol edelim. 

![hogwarts2](https://user-images.githubusercontent.com/55113204/126190948-22d44d73-ee86-4e85-be02-213890780ea7.png)

Bizi Apache bilgisi veren bir sayfaya yönlendirdi. Peki o zaman Ctrl+u ile source koduna bakalım.

![hogwarts3](https://user-images.githubusercontent.com/55113204/126191513-27a88ba7-dde2-440e-8786-2649e8dfe6fd.png)

Böyle zamanlarda genelde /html ile biten sayfaların altında devam eden bir takım kodlar varsa o kodlar muhtemelen bizim işimize yarar. O zaman bu /alohomora alıyorum bakalım neler
göreceğiz.

![hogwarts4](https://user-images.githubusercontent.com/55113204/126191994-fa1ab913-363b-4b36-aa8d-2925449e7718.png)

Aaaa password Draco'nun eviymiş, orası neresiymiş bir bakalım.

![hogwarts5](https://user-images.githubusercontent.com/55113204/126192297-f020f3d4-8fa8-4720-9139-57b9db744e42.png)

Slytherinmiş. Hadi bakalım bu bilgiyle neler yapabileceğimizi düşünelim. İlk bir nikto aracını kullanarak güvenlik zaafiyetlerini ve içerisinde işimize yarayacak bilgiler barındıran 
klasörleri bulabilecek miyiz?

![hogwarts6](https://user-images.githubusercontent.com/55113204/126197705-715a0cd3-dcee-4306-b17c-70d9efb8efbe.png)

Bi bakalım /phpinfo.php dosyasına ne çıkacak.

![hogwarts7](https://user-images.githubusercontent.com/55113204/126198309-9071f4b6-03e0-4e20-89a9-36b83f53a7cc.png)

Bir şey çıkmadı. Bunu geçelim başka hangi aracı kullanabiliriz hımmm, Bir dizin keşfi yapan burte-force (kaba kuvvet) saldırı programı olan gobuster aracını kullanalım bakalım.

![hogwarts8](https://user-images.githubusercontent.com/55113204/126198889-1f39abe7-cc98-405a-97ed-5ed5bc787cf7.png)

Şimdi bakalım bu çıkan gizli dizinlere.

![hogwarts9](https://user-images.githubusercontent.com/55113204/126199065-bc56cca5-b162-4e79-991d-98cfa3943ab0.png)

Yeap ilk flag kaptık. Bunu kaydedelim bir yere. Bakın bizi başka bir dizine de yönlendiriyor. Ona girelim bakalım.

![hogwarts10](https://user-images.githubusercontent.com/55113204/126199337-3a4857da-a97b-4862-89ad-b630b0f71b58.png)

AVADA KEDAVRA!!! öyle mi :D tatlı olmuş bence. Bu arada dobbyde çıkan brainfuck  Urban Müller tarafından yaratılmış bir programlama dilidir. Yaratılma amacı mümkün olan en 
küçük boyutlu derleyiciyi üretmektir. Bilinen bazı derleyicileri 200 bayttan küçüktür. Online compiler kullanarak bakalım ne diyormuş.

![hogwarts11](https://user-images.githubusercontent.com/55113204/126199990-698353cf-1fb0-46ec-988f-39115ee78e73.png)

![hogwarts12](https://user-images.githubusercontent.com/55113204/126200587-9cf2f09d-b130-444e-b664-32dd61810c8f.png)

Sayfanın bir de wordpress olduğunu öğrendik. Bakalım neler login olabilecek miyiz?

![hogwarts13](https://user-images.githubusercontent.com/55113204/126201459-306eab39-2cfa-4780-a944-341b68fa993b.png)

Evet wordpressin login sayfasına ulaştık. Kullanıcı adımız draco idi parolamızda Slytherindi deneyelim. Parola büyük harf kabul etmiyor ondan küçük harfle deneyelim ve içeri 
girelim. Ama yinede kullanıcı adımızı bilmiyor olsaydık WPScan aracı, bir WordPress sitesinde kulllanılan eklentileri ve temaları bulmak, bir WordPress sitesine Brute force 
saldırısı yapmak gibi çeşitli alanlarda kullanılabiliriz. Hadi onu da öğrenelim.

![hogwarts14](https://user-images.githubusercontent.com/55113204/126202458-bb68ae29-6fbf-4970-8ab0-1b4d4e945180.png)

![hogwarts15](https://user-images.githubusercontent.com/55113204/126202466-1084c355-37be-4edb-8c89-2baac8e75e53.png)

Bu şekilde draco olduğunu öğrenebiliriz yine. Şimdi içeri girelim. 

![hogwarts16](https://user-images.githubusercontent.com/55113204/126202684-4f8d825e-3e0f-4775-9de1-b9002ba14ea4.png)

Şuanda adminiz bakalım neler yapabileceğiz burada. Plug üzerinden reverse shell yapalım.Plug-in, kendi başına çalışabilen bir program için, genellikle çok özel bir alanda 
duyulan gereklilik üzerine geliştirilen, programa yeni özellikler ekleyen yazılımdır. Plug-inler ana programdan bağımsız çalışamaz. Uygulamalar çok çeşitli nedenlerden dolayı 
plug-inlere destek verirler.

![hogwarts18](https://user-images.githubusercontent.com/55113204/126223536-4c1df0ef-c355-40db-a5ed-472307544b9c.png)

Bu temayı kullandığı için bizde bu temayı indirelim.

![hogwarts17](https://user-images.githubusercontent.com/55113204/126223594-b9c6844c-3327-4285-99a3-7be45b7bafab.png)

Burada şifreyi görüyorum.

![hog](https://user-images.githubusercontent.com/55113204/128427950-b4464ae1-993e-4e6e-b3f5-7062d399c81a.png)

Çözmek için hangi yöntemi kullanacağımıza bakalım.

![hog2](https://user-images.githubusercontent.com/55113204/128427956-3780d256-3701-4708-9ab6-2ab3d7fe8454.png)

Girişte gördüğümüz kodu çözelim.

![hog3](https://user-images.githubusercontent.com/55113204/128427969-291a2c97-b192-44d9-9975-0c5d0b6c1850.png)

WpScan aracı kullanarak wordpress zaafiyetlerini tarayabiliriz.

![hog4](https://user-images.githubusercontent.com/55113204/128427984-41c59804-ae1d-48d4-8917-6f5dff469d14.png)

Draco kullanıcısının index oflarına ulaştım.

![2021-08-06_011634](https://user-images.githubusercontent.com/55113204/128428390-1493028f-35d8-43a7-9ac2-d4f392c1ff2b.png)


**¯\\\_(ツ)\_/¯**
















