## KRİPTOLOJİ NEDİR?

Kriptografi bilginin yada mesajın anlamını gizlemek amacıyla çeşitli şifreleme yöntemleri ile verinin işlenmesidir diyebiliriz. O zaman hadi çeşitli kriptoloji algoritmalarını 
öğrenelim.


## SİMETRİK KRİPTOGRAFİ

Şifreleme ve şifre çözmek için ortak anahtar kullanılmaktadır. 

![9](https://user-images.githubusercontent.com/55113204/125139205-cb3a6a80-e118-11eb-84c9-575110c46af6.PNG)


## DES ALGORİTMASI

Des algoritması ilk simetrik şifreleme algoritması olarak bilinmektedir. Bir veriyi belirli bloklara bölerek o şekilde şifreleme gerçekleştirir.Daha sonra şifreleme yaptığı
blokları birleştirmektedir. Yani kısacası bir blok şifreleme algoritmasıdır. Key uzunluğunun kısa olması sebebiyle pek güvenli olduğu söylenemez. Simetrik şifrelemelerde en önemli
nokta key ve key uzunluğudur. DES algoritmasının blok uzunluğu 64 key uzunluğu 56 bittir. Brute Force saldırıları ile DES algoritmasının keyleri tahmin edilebilmektedir.

Simetrik şifreleme algoritmasının kullanımında bir anahtar ile veri şifrelenir ve şifrelenmiş metin elde edilir. Sonrasında bu şifrelenmiş metini çözmek için yine aynı anahtarı 
kullanırız. Bu sebepten dolayı anahtarın gizliliği çok önemlidir ondan dolayı dikkatlince korunmalıdır. Güvenlik açısından zayıf olmasının yanı sıra hızlı çalışan bir algoritmadır.

![1](https://user-images.githubusercontent.com/55113204/125104132-b8f30900-e0e5-11eb-8e18-ac55ff649a1b.jpg)

DES Algoritmasında matematiksel 1 ve 0 lar üzerinden gerçekleştirilir. Yani Bitler üzerinden gerçekleştirilmektedir. Genel olarak işlemi süreci aşağıdaki gibidir.

![2](https://user-images.githubusercontent.com/55113204/125106208-0f614700-e0e8-11eb-98c0-8bda45c00fa6.PNG)


Şimdi adım adım ilerleyelim. İlk olarak Initial Permutation işlemine bakalım. Bu adım DES Algoritmasının ilk adımınıdır. Dışarıdan gelen 64 bitlik açık karışık olarak indislenir.
Normalde indisler 1 2 3 ... şeklinde sırasıyla gitmesi gerekirken bu indisler karışık olarak yerleştirilir.

![3](https://user-images.githubusercontent.com/55113204/125107697-c7432400-e0e9-11eb-8738-948c0de71634.PNG)

Daha sonrasında initial permutation kısmından gelen veren 32 bitlik sağ ve sol olmak üzere ikiye ayrılıyor. 

![4](https://user-images.githubusercontent.com/55113204/125113177-f7da8c00-e0f0-11eb-92b8-3244053fd0fe.PNG)

![5](https://user-images.githubusercontent.com/55113204/125115709-610fce80-e0f4-11eb-9ae6-f587640c9ad6.PNG)

6 bit girip nasıl 4 bit çıktığına birlikte bakalım.

![7](https://user-images.githubusercontent.com/55113204/125137990-75fd5980-e116-11eb-9aee-625a2f62af85.PNG)

![8](https://user-images.githubusercontent.com/55113204/125138677-bdd0b080-e117-11eb-9d73-bbc85d5d7982.PNG)

Bu şekilde 16 kere döngüye girmektedir.

### TRIPLE DES (ÜÇLÜ DES ALGORİTMASI)
DES Algoritmasının 3 kez farklı anahtarlar ile çalıştırılmasında Triple DES Algoritması denir.
Üçlü DES Algoritmasında ilk olarak 1. anahtar ile veri şifreleniyor. Daha sonra 2. anahtar ile şifre çözümü gerçekleştiriliyor ve son olarak 3. anahtar ile tekrar şifreleniyor.
Tabiki burada 3 anahtar da birbirinden farklıdır. Şifre çözümü de tersten işliyor. İlk olarak şifrelenmiş veri 3. anahtar ile çözülüyor. Sonra 2. anahtar ile şifreleniyor ve
tekrar 3. anahtar ile şifre çözülmektedir. Sistem bu şekilde ilerlemektedir.

![6](https://user-images.githubusercontent.com/55113204/125137172-d4293d00-e114-11eb-93a5-6c5f8bfb87ba.PNG)


## AES ALGORİTMASI

Simetrik algoritmalardan bir diğeri ise AES Algoritmasıdır. Brute force saldırılarına dayanıklı bir algoritmadır.Bu Algoritma 128 bit bloktan oluşmaktadır. Yani giriş ve çıkış 
128 bitten oluşmaktadır. Girişteki herbir bayt 4x4 AESdurum matrisinin bir hücresine yerleştirilmektedir. En sonunda da elde edilen bayt değerleri birleştirilerek algoritma 
elde edilmiş oluyor. 
128 bit, 192 bit, 256 bit olmak üzere 3 farklı anahtar uzunluğuna sahiptir. 4 fonksiyonlu tur algoritmasından oluşur ve tur sayısı da anahtar uzunluğuna bağlı olarak 10, 12, 14
tur olarak değişmektedir. 

![11](https://user-images.githubusercontent.com/55113204/125142107-9da4ef80-e11f-11eb-949d-aa102ab68c34.PNG)


![12](https://user-images.githubusercontent.com/55113204/125142123-a8f81b00-e11f-11eb-9514-750e54e28c70.PNG)


### SubBytes Dönüşümü

Subbytes dönüşümündeki sol taraftaki kutucuklar içinde her bir bayta sağ taraftaki tabloya göre dönüşüm gerçekleştirir. Örnek olarak S0,0 giriş matrisinin değeri hexadecimal 
olarak 53 olsun. Sağ taraftaki tabloda satırdan 5, sütundan 3'ü işaretleyip bu iki sayının gösterdiği ed değeri bizim yeni durum matrimizdir. Sağ taraftaki tablo rastgele
oluşturulmuyor içerde matematiksel işlemler sonucunda bu tablo değerleri elde edilmektedir.

![13](https://user-images.githubusercontent.com/55113204/125142072-8534d500-e11f-11eb-9ccc-8b25e98c81f1.PNG)

### ShiftRows Dönüşümü 

Bu dönüşümde durum matrisindeki satırlar dairesel döndürmeye tabi tutulmaktadır. İlk satır aynnı kalır ama diğer satırlar da döndürme işlemi gerçekleştirilir. 2. satır sola doğru
1 birim döndürülür. 3. satır sola doğru 2 birim döndürülür. Son olarak da 4. satır sola doğru 3 birim döndürülmektedir. Aşağıdaki görselde bunun örneklendirilmiş hali mevcuttur.

![14](https://user-images.githubusercontent.com/55113204/125142402-4fdcb700-e120-11eb-80aa-a28c18b5652c.PNG)


### MixColumns Dönüşümü

Burada satırlar üzerinde değil sütunlar üzerinde işlem yapılmaktadır. Sağdaki durum matrisindeki her bir sütunu alıp sol üstteki matris ile çarparız. Bu işlem bütün sütunlar için
yapılır.

![15](https://user-images.githubusercontent.com/55113204/125142740-1f494d00-e121-11eb-91f1-542afb502fae.PNG)


### AddRoundKey Dönüşümü

Durum matrisindeki her bir sütunu tur anahtarını içeren matristeki her bir sütun ile logic xor işlemine tabi tutulmasıdır. Bu dönüşümün tersi de kendisi ile aynı olur.

![16](https://user-images.githubusercontent.com/55113204/125142790-3ee07580-e121-11eb-92e8-a5a9d0e8a263.PNG)

### Key Expansion

Tur anahtarlarının hesaplanmasıdır. Cipherkey burada bize ilk tur anahtarını ifade etmektedir. Sıradaki tur anahtarının hesaplanması ise önceki tur anahtarının son sütunu
shiftrows dönüşümündeki gibi dairesel dönüşüme tabi tutulur. Elde edilen sütunun bütün hücreleri s box tablosundaki dönüşümden geçmektedir. Yani buradaki SW dönüşümden geçmiş
olarak düşünebiliriz. Sonrsında bu sütun değeri Rcon değeri ile xor yapılır. Burada kullanılan Rcon'un ilk değeri 01000000'dır. İkinci Rcon değeri ise 02000000'dır. Bu şekilde 
2'yekatlanarak devam etmektedir. Rcon işleminden sonra, önceki tur anahtarının ilk sütunu ile xor işlemi yapılır. Bunun sonucunda ilk tur anahtarının ilk sütunu oluşmuş olur. 
2. sütunu ise yeni oluşmuş tur anahtarının ilk sütunu ile bir önceki tur anahtarının 2. sütunu xor işlemine tabi tutulması ile gerçekleşir. Bu şekilde devam edilir. 

![17](https://user-images.githubusercontent.com/55113204/125142978-ce862400-e121-11eb-8670-3b01596f45ef.PNG)


## ASİMETRİK KRİPTOGRAFİ

Bu algoritmaya göre public ve private olmak üzere farklı anahtarlar mevcuttur. Herkeste tüm anahtarlar yoktur. Bunun yerine anahtarlar paylaştırılmıştır. Özetle anlatmak 
gerekirse bir veriyi şifrelemek için bir public anahtar gerekir bu herhangi bir kişi tarafından bilinebilir. Ancak bu şifrenin çözümü ise sadece secret key yani gizli anahtar 
ile gerçekleştirilmektedir.

![10](https://user-images.githubusercontent.com/55113204/125143966-09d62200-e125-11eb-9586-0dbce83e0b7c.PNG)

### Kriptografi 3 önemli yapıtaşından oluşmaktadır. 

*** Confidentiality (Gizlilik)
*** Data Integrity (Veri Bütünlüğü)
*** Authentication (Kimlik Doğrulama)


## RSA ALGORİTMASI

Genel olarak şifrelenmesi asal sayılar üzerinden gidilerek yapılmaktadır. Gizli p ve q isminde büyük değerli asal sayılar seçilir. Daha sonra e sayısı belirlenir ki bunun şartı
ise p x q dan küçük olan ve (p-1) x ( q-1) değeri ile aralarında asal olan sayı e sayısı olarak seçilir. Daha sonra d gizli parametresi oluşturulur. Bunun için ise; 
mod (p-1) x (q-1) e göre e değerinin tersidir. 

![18](https://user-images.githubusercontent.com/55113204/125144773-97b30c80-e127-11eb-8dfc-adc8edddbaf9.PNG)



## TEK YÖNLÜ FONKSİYONLAR

## SHA2 ALGORİTMASI

Tek bir algoritma değildir. İçinde 6 farklı algoritmaya sahiptir. SHA (Secure Hash Algorithm) algoritması ismini çıktı uzunluğundan alır. Yani SHA256 algoritması 224 bittir.
SHA224 ve SHA256'da 512 bitlik girişler işlemlere tabi tutulur. 16x32'lik diziler olmak üzere 8 parçaya bölünür. Ve bu parçalara işlemler başlatılır. Daha sonrasında 512 bitlik işlem blogunun sonuna işlemin boyutu mesaj olarak eklenir. Bu SHA224 ve SHA256 algoritmasında işleme giren kısıma "chunk" denir ve her bir chunk 64 hashi döngüde hesaplanmaktadır. Eğer blok 512 bitten küçük ise blok sonuna padding (ekleme) işlemi yapılmaktadır. 508 bitlik bir blok varsa bunun son 4 biti 1000 şeklinde padlenir. Yani ilk olarak 1 koyulur geriye kalanlara da 0 eklenir. Bunun sebebi 512 bite tamamlamaktır. 

![hash](https://user-images.githubusercontent.com/55113204/125205300-42434080-e28a-11eb-99c8-1187de361abf.PNG)

## SHA3 ALGORİTMASI

SHA Algoritmalarının en güvenilir ve en güncel olan versiyonudur. İç yapısı olarak SHA1 ve SHA2 den farklı olarak yapılmıştır. Bu algoritma ayrıca saniyedeki çıktı sayısının yüksek olması düşük enerji tüketmesinden dolayı tercih edilmektedir. SHA3 Algoritmasında sponge method (sünger methodu) kullanılmıştır. 
Temel olarak Absorbing (durum sönümleme) ve Squeezing (sıkıştırma) olmak üzere iki durumdan oluşmaktadır.

![has2](https://user-images.githubusercontent.com/55113204/125206345-779e5d00-e28f-11eb-9eef-1d49fea0bdaf.PNG)

Aslında r ve c toplam boyutu her zaman 1600 bite eşittir. Ama işleme giren mesaj boyutu r dğerine eşit olmak zorundadır. Bu demek oluyor ki chunk boyutu çıktı boyutuna göre değişmektedir. 

![has3](https://user-images.githubusercontent.com/55113204/125206097-08743900-e28e-11eb-94a8-eaeb34fd5d60.PNG)

Fonksiyon sonucunda çıkan çıktının tersinin elde edilmesi zor olmasından ve her sonucun aynı algoritma için aynı boyutta çıkması için hash fonksiyonlarının güvenliği önem kazanmıştır. 

Veri bütünlüğünü doğrulama, verinin tam alındığını onaylamak için checksum karşılaştırması, digital imzalar, blockchain teknolojileri en çok kullanılan kullanım alanlarıdır.

Bu algoritmaya yapılan saldırılardan biri dictionary (sözlük) saldırılarıdır. Eğer sizin elinde bir SHA256'nın bir hash değeri varsa, bu hash değerini sözlük içinde arattığınızda tersini bulmanız mümkündür. Bundan dolayı karmaşık şifreler koymak önemlidir.

Diğer bir saldırı ise brute force (kaba kuvvet) saldırılarıdır. Bu saldırılarda elimizde bir özet değeri vardır. Bu özet değerleri çeşitli CPU ve GPU'larla çok fazla özet değeri girdileri ile karşılaştırılır. Bu saldırı çeşidinde önemli olan şey işlemi gerçekleştiren işlemcinin ne kadar güçlü olmasıdır. Bu işlem MD5 gibi 128 bitlik çıkışı olan, günümüz şartlarında küçük çıktı boyutu olarak kabul edilen algoritmalar için kabul edilmektedir. 256 bit ve fazlası olan çıktısı olan algoritmalarda başarılı olması zordur. 

Collusion (çarpışma) atakları, her ne kadar düşük ihtimal de olsa iki farklı girdinin özet değerlerinin aynı olma olasılığından doğan ataklardır. Çarpışma olasılıklarını azaltmak için çeşitli matematiksel yöntemlerden en basiti olarak çıkıştaki bit sayısını arttırmaktadır. 






**¯\\\_(ツ)\_/¯**













