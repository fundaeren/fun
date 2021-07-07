
## KIOPTRIX LEVEL 1 WALKTHROUGH

### YÖNTEM 1 SMB KULLANARAK DOSYA AKTARIMI 
Selammm :) Yeni bir makine çözmeye hazır mısınız? O zaman hemen başlayalım.

İlk olarak hedef makineyi çalıştırıyoruz.

![1](https://user-images.githubusercontent.com/55113204/124664987-d9884c80-deb4-11eb-804c-b449b10e8bcb.PNG)

Daha sonra netdiscover aracı ile hedef makinenin ip adresini öğrenelim.

![2](https://user-images.githubusercontent.com/55113204/124665114-00468300-deb5-11eb-9cff-5b7f4cb5399e.PNG)

Daha sonra makineye port ve servis taramasını ayrıntılı olarak bakalım. -O burada işletim sistemini öğrenmek istediğimiz yazıldı.

![3](https://user-images.githubusercontent.com/55113204/124666138-4223f900-deb6-11eb-9f20-8d7e31fcc810.PNG)

Metasploit kullanarak smb versiyon bilgisini elde etmeye çalışalım.

![Ekran Alıntısı](https://user-images.githubusercontent.com/55113204/124668876-2d496480-deba-11eb-8638-572a1ccb10c2.PNG)


Smb ile ilgili ne yapacağımıza karar vermek için tüm exploitleri getirelim.

![kriptox2](https://user-images.githubusercontent.com/55113204/124668885-30dceb80-deba-11eb-871b-ac72d30f9b40.PNG)

![kriptox3](https://user-images.githubusercontent.com/55113204/124668900-34707280-deba-11eb-8296-6bded28078ff.PNG)
Hadi birlikte searchsploiten exploit kodunu bulup derleyip çalıştırıp shell alalım.
Tamamdır versiyonu aldık şimdi bu versiyon bilgisini aratmamız gerekiyor. Bu versiyonun açıklarını searchsploit kullanarak Localde arayalım. 

![kriptox4](https://user-images.githubusercontent.com/55113204/124669583-4ef71b80-debb-11eb-94e5-71d1d28e8447.PNG)

Burada searcsploit -x ile exploitin içini detaylı görebilmekteyiz.

![kriptox5](https://user-images.githubusercontent.com/55113204/124670096-27ed1980-debc-11eb-9760-e9d479ffc5ab.PNG)

![kriptox6](https://user-images.githubusercontent.com/55113204/124670204-51a64080-debc-11eb-8e41-4bbfe1f76e18.PNG)

Daha sonra incelediğimiz içeriği Q ile çıkış yapıyoruz ve -m parametresi ile tekrardan kaydedelim. Çünkü bu exploit bizim işimize yarayacak gibi.

![kriptox7](https://user-images.githubusercontent.com/55113204/124670644-f3c62880-debc-11eb-8784-a746dbc32627.PNG)

Bu exploiti gcc ile kullanabilir hale getirmek için derleyelim. Sonrada çalıştıralım.

![kriptox8](https://user-images.githubusercontent.com/55113204/124670711-0fc9ca00-debd-11eb-9c4e-1d6195f34608.PNG)

Burada brute forse yapmak için -b ve linux olduğu için 0 kullanacaz. Geri dönüş bize olacağı için kendi ip adresimiz ve hedef makinenin ip adresi ile shell almaya çalışalım. Gördüğünüz üzere rootuz.

![kriptox9](https://user-images.githubusercontent.com/55113204/124671145-bc0bb080-debd-11eb-8be8-1ee5b7310655.PNG)

Ben burada smbex in adını smbsearch.c olarak değiştirdim çünkü 10.c olarak kaydolan dosya .c uzantısı ile çalışmaktadır sizde öyle yapın lütfen. Kendi makinemde dosya çekebilmek içim HTTPServerı etkin hale getirdim. Daha sonrasında wget ile hedef makinenin içindeyken kendi makinemdem dosya 10.c dosyasını çekebildim.

![kriptox10](https://user-images.githubusercontent.com/55113204/124674820-26bfea80-dec4-11eb-84ab-399da9355b54.PNG)

Çektiğimiz dosyayı da http üzerinden görebiliriz.

![kriptox11](https://user-images.githubusercontent.com/55113204/124675017-81594680-dec4-11eb-927d-e7d40b38c0ef.PNG)

### YÖNTEM 2 METASPLOİT KULLANARAK DOSYA AKTARIMI

Şimdi Metesploit kullanarak shell alalım. Ve buradaki trans2open exploitini seçiyorum.

![k2_1](https://user-images.githubusercontent.com/55113204/124677723-b9af5380-dec9-11eb-8e54-ccb0983b463d.PNG)

Reverse shell için bir payload seçiyorum ve exploit diyip shell alıyorum.

![k2_2](https://user-images.githubusercontent.com/55113204/124678664-aa310a00-decb-11eb-8360-34879892c006.PNG)

![k2_3](https://user-images.githubusercontent.com/55113204/124678745-d9e01200-decb-11eb-9fa5-f59b9daa34d6.PNG)











