## FIRST BLOOD WALKTHROUGH

Merhaba bugün yeni bir makine olan first blood makinesinin çözümünü birlikte gerçekleştireceğiz. Hadi başlayalım o zaman :)

İlk önce hedef makinemizin ip adresini öğrenelim. Bunun için ben netdiscover aracını kullanıyorum genellikle.

![first_blood_1](https://user-images.githubusercontent.com/55113204/124729246-f22a4e00-df18-11eb-9e8d-355f6ea1a31e.PNG)

Görüldüğü üzere ip adresimizi bulduk. Şimdi bu makinenin açık portlarını bu portlarda çalışan servislerini ve işletim sistemini öğrenelim. Bunun için nmap aracını nmap aracını kullanabiliriz.

![first_blood_2](https://user-images.githubusercontent.com/55113204/124729712-5baa5c80-df19-11eb-9597-eaa8ded058fb.PNG)

HTTP 80 ve SSH 60022 portlarının açık olduğunu gösteriyor. İlk olarak 80 portundan ilerleyelim bakalım. 80 portunu tarayıcıda ip adresinin sonuna :80 olarak yazalım ve karşımıza bir sayfa çıkacak mı bakalım.

![first_blood_3](https://user-images.githubusercontent.com/55113204/124831724-4d455a80-df84-11eb-8537-184629523a6e.PNG)

Yeap çıktı. Güzeeell !! Bizi kendi yönlendiriyor. Sayfanın source bakalım bakalım o zaman.

![first_blood_4](https://user-images.githubusercontent.com/55113204/124832067-c0e76780-df84-11eb-8ef6-d72b3d7b16cc.PNG)


Gördüğünen o ki yönlendirmeler yeni başlıyor :D Hadi dediğini yapalım ve rambo.html'e gidelim.


![first_blood_5](https://user-images.githubusercontent.com/55113204/124832057-bc22b380-df84-11eb-8d6b-09cdcf3d7585.PNG)

Dediğini yapalım hedef makinemizin ip adresi üzerinde nikto aracını kullanalım.

![first_blood_6](https://user-images.githubusercontent.com/55113204/124832353-3a7f5580-df85-11eb-826e-436e3a847c66.PNG)

HOOPP tekrar bir dizin çıktı ve içinde bu nedir diye tekrardan kontrol edelim mi?

UPPS bakın ne çıktıı :D

![first_blood_7](https://user-images.githubusercontent.com/55113204/124832422-5551ca00-df85-11eb-9961-562c0e8548cd.PNG)

Burada -d parametresi ile 1. derinliğine kadar inilerek incelenmesi, -m ile en az 5 karakter uzunluktaki kelimelerden oluşan sözlük oluşturması ve son olarak da -w ile words.txt isminde sözlük oluşturulmasını istiyor bizden. Peekkiğğğ o zamann

![first_blood_9](https://user-images.githubusercontent.com/55113204/124836950-8f729a00-df8c-11eb-849b-051cd6673a7b.PNG)

Robin Wood Really? :D

words.txt dosyası bittiği zaman ssh.html sayfasını ziyaret edin diyor.

![first_blood_8](https://user-images.githubusercontent.com/55113204/124836868-681bcd00-df8c-11eb-98f2-ea1e2f13bcde.PNG)

Şimdi ise hydra ile brute force saldırısı gerçekleştirmemizi istiyor. -l session open için, johnny kullanıcısı olduğu düşünülerekten words.txt içerisindeki kelimelerde parola olarak düşünülmüş. -s parametresi ile 60022 portuna ssh girişine kaba kuvvet saldırısı yapılmak hedefinde. -t de işi parçacıklara bölerek daha hızlı saldırının gerçekleşmesini sağlamakta.

![first_blood_9](https://user-images.githubusercontent.com/55113204/124837583-c2695d80-df8d-11eb-845b-9bd4b6f3da47.PNG)

Okey admin ve parola elimizde. 

![first_blood_10](https://user-images.githubusercontent.com/55113204/124838139-e8433200-df8e-11eb-927d-f39c0f8872f8.PNG)

Hadi ssh ile bağlanalım.

![first_blood_11](https://user-images.githubusercontent.com/55113204/124838776-3442a680-df90-11eb-9fc1-5178c825b725.PNG)

Ve olala içerdeyiz. Önce yetkimize bakalım.

![first_blood_13](https://user-images.githubusercontent.com/55113204/124839612-c39c8980-df91-11eb-8b4e-c7dc2685b6cb.PNG)

Şimdide neler diyor okuyalım bakalım.

![first_blood_12](https://user-images.githubusercontent.com/55113204/124839633-d1eaa580-df91-11eb-8c8f-df9026854867.PNG)

![first_blood_14](https://user-images.githubusercontent.com/55113204/124839760-0f4f3300-df92-11eb-9919-6f7bc01973fa.PNG)


html dizinine gitmemizi istiyorsa gideriz :))

![first_blood_15](https://user-images.githubusercontent.com/55113204/124839814-33ab0f80-df92-11eb-9955-8d21607f56b4.PNG)

Yine bir yönlendirme ve bir serverda bizim taraftan (client) okunan dosya gizlemiş onu find komutu ile bulmamızı istiyor.

![first_blood_16](https://user-images.githubusercontent.com/55113204/124840267-4114c980-df93-11eb-801f-0230017013fa.PNG)

Tamamdır tekrardan ssh ile bağlanabiliriz sunucuya 

![first_blood_17](https://user-images.githubusercontent.com/55113204/124840607-0eb79c00-df94-11eb-91be-db45b269bdff.PNG)

İşaretlediğim yerin açıklaması -u sly kullanıcısını gösteren parametredir. sly kullanıcısı /bin/cat dizini üzerinden /home/sly/README.txt çalıştırabilir.

![first_blood_18](https://user-images.githubusercontent.com/55113204/124841569-3871c280-df96-11eb-9122-57be03aec005.PNG)

Vee girelim bakalım.

![first_blood_19](https://user-images.githubusercontent.com/55113204/124841629-59d2ae80-df96-11eb-8aed-1a13d8c2682e.PNG)

![first_blood_20](https://user-images.githubusercontent.com/55113204/124841714-930b1e80-df96-11eb-9bb0-7f18d6ed20af.PNG)

sudo -l ile yetkilerin olanların dizinlerini bulalım. tüm hepsinde yetkili olan ftp imiş. Ve bizi simple komutlar ile shell almamızı sağlayan https://gtfobins.github.io/  sitesini kullanabileceğimizi söylemekte. Peki ftp ile nasıl shell alınıyor bakalım.

![first_blood_21](https://user-images.githubusercontent.com/55113204/124842392-1b3df380-df98-11eb-9742-e952600a97d8.PNG)

![first_blood_22](https://user-images.githubusercontent.com/55113204/124842497-52aca000-df98-11eb-9f4b-77d96ecaa622.PNG)

Görünen o ki artık root olduk. İşte makinenin sonuna geldik. Güzel bilgilendirici bir makineydi. Tabi yönlendirmesinden dolayı kolay oldu bizim için :D Ne diyelim, bir dahaki makinede görüşmek üzere o zaman byee :DD




¯\_(ツ)_/¯







