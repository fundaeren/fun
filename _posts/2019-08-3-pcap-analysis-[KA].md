# KALİ LİNUX KOMUTLAR PARAMETRELER VE GENEL BİLGİLER



# ls Komutu

ls komutu aktif olarak girmek istediğimiz dosyanın veya dizinin listelenmesini sağlayan komuttur. Bu komut sayesinde klasörlerin veya dizinlerin içerisinde neler var görebilmekteyiz.



# Parametreler

## -l Parametresi

Bu parametre ile dizinimizde bulunan dosya ve dizinlerin bilgilerini sırasıyla dikey ve ayrıntılı olarak öznitelikleri, sahibi, grubu, boyutu, update tarihi, ve dosya isimleri olarak bilgi verilmektedir. 

![image](https://user-images.githubusercontent.com/55113204/109417828-4905a100-79d6-11eb-9e68-57eb21a064b2.png)


## -a Parametresi

Bir dosya veya dizini yatay olarak listeleyen ve ayrıntılı bilgi veren parametredir. Ve gizli olan dosya ve dizinleri de göstermektedir.

![image](https://user-images.githubusercontent.com/55113204/109418294-bca8ad80-79d8-11eb-9ced-f12872a8b117.png)

## -al Parametresi

-al parametresi gizli olan ve sadece ls komutu ile gösterilmeyen dosyaların listelenmesini ve yatay ve dikey olarak ayrıntılı bir bilgi vermesini sağlamaktadır. Sırasıyla öznitelikleri, sahibi, grubu, boyutu, update tarihi ve dosya isimleri hakkında bilgi vermektedir.

![image](https://user-images.githubusercontent.com/55113204/109418090-90d8f800-79d7-11eb-852c-8d1726c12433.png)

## -alrt Parametresi

Değiştirilme zamanlarına göre listeleme yapan parametredir.

![image](https://user-images.githubusercontent.com/55113204/109418204-27a5b480-79d8-11eb-97c6-90e78c5c1ea1.png)

## -l -h Parametresi

Hem kb,mb,gb gibi boyut değerleri ile hemde dikey ve ayrıntılı şekilde dosya veya dizin hakkında bilgi vermektedir.

![image](https://user-images.githubusercontent.com/55113204/109418226-4d32be00-79d8-11eb-8bec-0f744e6cd565.png)

## -o Parametresi

-h parametresi gibi dosya ve dizini listeleyen fakat boyutlarını göstermeyen, aynı zamanda farklı kullanıcı grubu olduğunda onları göstermeyen parametredir.

![image](https://user-images.githubusercontent.com/55113204/109418370-1c06bd80-79d9-11eb-87df-882ac0a67210.png)

## -l -t Parametresi

Dosya ve dizinleri dikey olarak ve time olarak listelemektedir. Son eklenen dosya veya dizin en üst sıradadır.

![image](https://user-images.githubusercontent.com/55113204/109418404-48223e80-79d9-11eb-8ab4-bc951d39950b.png)

## -l -t -r Parametresi

Burada zamana göre dikey ve ayrıntılı olarak listelenmektedir. Fakat reverse yani zamanı son eklenene göre değil ilk eklene göre listelenmektedir.

![image](https://user-images.githubusercontent.com/55113204/109418437-6f790b80-79d9-11eb-8140-73ca727224a6.png)

## -l -r Parametresi

Dosya ve dizini ayrıntılı olarak dikey olarak alfabetik olarak listeler ama reserve parametresi ile tersten sıralamaktadır.

![image](https://user-images.githubusercontent.com/55113204/109418504-bc5ce200-79d9-11eb-869d-bb95e2880789.png)

## -l -d Parametresi

Sadece bulunduğumuz dizin hakkında ayrıntılı bilgi vermektedir. Biz burada belgeler dizinindeyiz içindeki dosyaları görememekteyiz.

![image](https://user-images.githubusercontent.com/55113204/109418533-e1e9eb80-79d9-11eb-8251-a4ba338c8479.png)

## -l listelenmek_istenen1 listelenmek_istenen2 Parametresi

İki veya daha fazla dizini aynı anda dikey ve ayrıntılı olarak listeleyebiliriz.

![image](https://user-images.githubusercontent.com/55113204/109418551-fc23c980-79d9-11eb-8fa2-c6c331efdc5a.png)

## -i Parametresi

Dosyaların index bilgilerini küçükten büyüğe doğru sıralamaktadır.

![image](https://user-images.githubusercontent.com/55113204/109418558-1198f380-79da-11eb-94eb-111687840458.png)

## --sort=? Parametresi

Sıralama soru işareti yazılan yere gelen parametreye göre büyükten küçüğe göre yazılır. Extension, size, time, version veya none olarak değerler yazılabilir.

![image](https://user-images.githubusercontent.com/55113204/109418585-3e4d0b00-79da-11eb-9d27-478e2b42c7eb.png)

## -I ? Parametresi

Soru işareti ile belirtilen alana gösterilmesini istemediğimiz klasörü yazdığımızda ayıklayarak listeliyoruz.

![image](https://user-images.githubusercontent.com/55113204/109418611-60df2400-79da-11eb-8e9e-5c804ea93f0f.png)

## -R Parametresi

Alt dizinleri listelemektedir.

![image](https://user-images.githubusercontent.com/55113204/109418626-75bbb780-79da-11eb-9698-8d50179279f0.png)

## -1 parametresi

Her satıra 1 dosya yazılarak listeleyen komuttur.

![image](https://user-images.githubusercontent.com/55113204/109418635-83713d00-79da-11eb-9f9d-144593f4b9ec.png)

## - -v Parametresi

Version bilgilerini göstermektedir.

![image](https://user-images.githubusercontent.com/55113204/109418647-9be15780-79da-11eb-8d2e-4880b0c986d4.png)

## - -help Parametresi

ls komutu ile ilgili daha fazla bilgi edinmek için help komutu kullanılmaktadır.

![image](https://user-images.githubusercontent.com/55113204/109418657-b3b8db80-79da-11eb-8abc-8fa58581ba26.png)



# whoami Komutu

Ben kimim komutudur. Who am i yani aktif user kim onu gösterir. Bu komut yerine id -un komutu da kullanılabilmektedir. Burada biz kullanıcının funda olduğunu görmekteyiz.

![image](https://user-images.githubusercontent.com/55113204/109419299-c8e33980-79dd-11eb-9d5f-50dd83fcb4de.png)

# tar Komutu

Arşivleme yapan komuttur. Burada -c parametresi ile tar arşivini create eder. -f ile de izin verir.

![image](https://user-images.githubusercontent.com/55113204/109419322-e31d1780-79dd-11eb-8116-b6e65217b076.png)

-x parametresi var olan arşivi aç
-t parametresi tar arşivinin içeriğini listele
-v parametresi kullanıcıya neler olduğunu anlat
-r parametresi arşivi addle
-u parametresi arşivi updatele
-z parametresigzip/gunzip kullanarak sıkıştırma yap
-remove parametresi arşivle işin bitince sil

# Gzip/guzip Komutu

Dosyaları gziple ve guziple arşivler.

![image](https://user-images.githubusercontent.com/55113204/109419343-0051e600-79de-11eb-87a7-9737b91a5357.png)

-l parametresi sıkıştırılmış dosyanın içeriğini listeleler.
-f parametresi dosyalar açılırken benzerleri varsa üstüne yazar.

![image](https://user-images.githubusercontent.com/55113204/109419347-09db4e00-79de-11eb-8440-06f3c9c1ca52.png)

# apropos Komutu

bBir komutun ne işlev yaptığını bilindiği ama komutun ne olduğunu unuttuğumuzda apropos komutu kullanılır. Misal sistemin ne olduğunu biliyorum ama ne işe yaradığını bilmiyorsam burada apropos komutu kullanabilirim.

![image](https://user-images.githubusercontent.com/55113204/109419373-2b3c3a00-79de-11eb-8178-62b50c192cce.png)

# cat Komutu

Bir metin dosyasının içerisinde neler var onları görüntülemek için kullanılan komuttur.

## -n Parametresi 

-n parametresi ile her satırı ekrana bastırır.

![image](https://user-images.githubusercontent.com/55113204/109419417-6b032180-79de-11eb-902e-dda8ed623941.png)

## -E Parametresi

-E parametresi ile her satırın sonuna $ işareti koyar.

![image](https://user-images.githubusercontent.com/55113204/109419439-83733c00-79de-11eb-878e-5ecd03f29037.png)

# mkdir Komutu

Dizin yani klasör oluşturma komutudur. Biz burada fundaa isimli bi dizin oluşturduk ve -ls komutu yardımı ile görüntüledik. 

![image](https://user-images.githubusercontent.com/55113204/109419463-9f76dd80-79de-11eb-9cdb-e0327c664722.png)

# cp Komutu

Copy paste yani bir dosyayı yada klasörü kopyalamak istenildiğinde kullanılan komuttur. 
-r parametresi ile kullanılır sebebi ise dizinin içindeki her şey gösterilen hedef dizine kopyalanır. funda_deneme isimli dizini bulunduğu konumdan belgelere kopyaladım.

![image](https://user-images.githubusercontent.com/55113204/109419499-d51bc680-79de-11eb-9cc2-d2f40a10cd0e.png)

-d paratmetresi dosyanın aslını değil linkini kopyalamaktadır.
-p parametresi ile dosyanın kullanıcı izinlerini ve passwordlarını koruyarak kopyalanmasını sağlamaktadır.
-a parametresi diğer parametrelerle aynı kullanımdadır.
-f parametresinde kullanıcıya hiçbir izin sorusu sorulmadan kabul edilmiş olarak düşünülerek varsa aynı dosyadan silinip tekrardan kopyalanmasını sağlayan değerdir.
-i hedef adreste dosya mevcut ise kullanıcıya bilgi sorulur.
-u parametresinde kopyalanacak dosyanın tarihi eski dosyadan daha yeni ise bir nevi güncel ise kopyalanmaktadır.
# cat Komutu

Cat komutu ile dosya oluşturulup dosya içeriği okunabilmektedir. Text ve script dosyalarını okuyabilmemizi sağlamaktadır. Burada deneme adında bir dosya oluşturduk ve dosyanın içine Ankara ve Istanbul isminde iki bilgi girdik. Cat komutu ile hem dosyayı oluşturabildik hemde içeriği görüntüleyebildik.

![image](https://user-images.githubusercontent.com/55113204/109419537-ff6d8400-79de-11eb-8aa0-27f2a2fb3fb5.png)

Cat ile dizinlerin içine girmeden direk home üzerinden istenilen hedefe dosya oluşturulabilir.

![image](https://user-images.githubusercontent.com/55113204/109419542-085e5580-79df-11eb-8af5-83daf27a27d3.png)

Cat ile bir dizinin sonuna ekleme yapılarak update yapılabilir.

![image](https://user-images.githubusercontent.com/55113204/109419546-0f856380-79df-11eb-81d6-f92389f8962f.png)

Cat komutu ile iki dosya farklı bir dosyada birleştirilme yapılabilir. Burada dosya1 ve dosya2 isminde iki tane dosya oluşturdum. Içine yazdığım bilgilerin birleştirmek için dosya3 adında dosya oluştururak görüntüledim.  E harfinden sonra boşluk bırakmadığımdan dolayı f harfiyle birleşti. Burada dosya birleştirdiğimizden dolayı arka arkaya geldiğini görmekteyiz
Satır numaraları ile görüntülemek için -n parametresi kullanmaktayız.

![image](https://user-images.githubusercontent.com/55113204/109419591-465b7980-79df-11eb-96b1-76b24a174486.png)

Dizinlerin içindeki tüm içerikleri görmek için “*” kullanılmaktadır.

![image](https://user-images.githubusercontent.com/55113204/109419604-5d9a6700-79df-11eb-87ec-46884a4e179b.png)

Cat hakkında daha fazla bilgi almak için - - h parametresi kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109419610-67bc6580-79df-11eb-8d94-805f67a70849.png)


# Mv Komutu

Mv komutu move yani taşıma yapmaktadır. Öncelikle taşınacak bir dosya oluşturuyoruz ki daha kolay anlayabilelim. Taşınacak yer adında bir dosya oluşturuyoruz. Dosyamızı buraya taşıyacağız sonra taşınıp taşınmadığını kontrol edelim.

![image](https://user-images.githubusercontent.com/55113204/109420954-4b6ff700-79e6-11eb-8b17-47eb0ddf7e21.png)

Tabi bunları yaparken hedef dizinde aynı isimde dosya var mı yok mu kontrol edilmelidir. Bu kontrol -i parametresi ile yapılmaktadır. Eğer aynı isimde bir dizin mevcut ise üzerine yazılsın mı diye bizden onay beklemektedir.

![image](https://user-images.githubusercontent.com/55113204/109420966-5d519a00-79e6-11eb-8e1b-b338da6866ac.png)
 
Mv komutu ile bir dosyanın uzantısını değiştirebiliriz. Masaüstünde bulunan fundaa isimli klasörü fundaa.txt metin dosyasına dönüştürebiliriz. Taşıma işlemi gibi önce değiştirilecek klasör ve sonra hangi tipe dönüştüreceğimizi belirleyip uzantısını ekleyerek yapmaktayız. Bu şekilde dosyanın adını da değiştirebiliriz. 

![image](https://user-images.githubusercontent.com/55113204/109420968-66426b80-79e6-11eb-89e2-c917a30c79a2.png)

## -n Parametresi

var olan dosyanın üzerine sorulmadan yazılmasını sağlamaktadır. Dosya taşındıktan sonra eski yerinden tamamen kaybolmuştur. Burada belgeleri masaüstüne taşıdık ve tekrar listelediğimizde taşındığını görmekteyiz.

![image](https://user-images.githubusercontent.com/55113204/109420984-765a4b00-79e6-11eb-9dc7-cecd585207ed.png)

# touch Komutu

touch komutu ile sıfır boyutlu dosya oluşturabiliriz. Burada kali isminde dosya oluşturduk.

![image](https://user-images.githubusercontent.com/55113204/109421013-8d993880-79e6-11eb-8ffa-ebc601dd6001.png)

Dosyaların isimlerini yan yana yazarak birden fazla dosya da oluşturabiliriz.

![image](https://user-images.githubusercontent.com/55113204/109421029-9c7feb00-79e6-11eb-948c-70c321398bff.png)

# stat Komutu

Bu komut sadece dosya adı ile dosyanın bilgilerini görüntülenmesini sağlamaktadır.

![image](https://user-images.githubusercontent.com/55113204/109421044-ab669d80-79e6-11eb-8deb-29074c05d48d.png)

# alias Komutu

Takma isim oluşturan komuttur. Isim = değer şeklinde syntax vardır.

![image](https://user-images.githubusercontent.com/55113204/109421058-bc171380-79e6-11eb-92fd-d40f225d6f55.png)

Kali de zip işlemi ziplenecek yer ve dosya olarak yazılır.

![image](https://user-images.githubusercontent.com/55113204/109421068-cdf8b680-79e6-11eb-9faa-5637e8797ef0.png)

Ziplediğimiz dosyanın içine -r parametresi ile özyinelemeli olarak yeni dizin ekleyebiliriz.

![image](https://user-images.githubusercontent.com/55113204/109421075-d9e47880-79e6-11eb-8ce4-e3956667b33c.png)

Cat komutu ile zipin içine bakalım.

![image](https://user-images.githubusercontent.com/55113204/109421081-e1a41d00-79e6-11eb-9d72-80031286a16a.png)

Unzip komutu ile zip olan bir dosyayı çıkartabiliyoruz.

![image](https://user-images.githubusercontent.com/55113204/109421085-e8cb2b00-79e6-11eb-9d80-4a0281069fd4.png)

-d parametresi ile farklı lokasyona zip dosyasını çıkartabiliyoruz.

![image](https://user-images.githubusercontent.com/55113204/109421091-ef59a280-79e6-11eb-9e30-0549a8824f35.png)

# chmod Komutu

Yetkilendirme izinleridir. Üç tip kullanıcı vardır u (user), g (group), o (other) olmak üzere bir de a (all) hepsini erişebilen bir kullanıcı vardır. Bunların yetkilendirilme tiplerine göre r (read), w (write) ve x (excute) olmak üzere 3 tür mevcuttur. Burada d dizinin de user rwx yani read,write,execute yetkisine, group xr (excute, read) yetkisine ve other x (excute) yetkisine sahiptir. ‘-’ tamamen yetkisiz olduğunu göstermektedir. D burada dizini temsil etmektedir. B özel blok sayfasını, c özel karakter dosyasını, l sembolik bağlantı dosyasını ve p ise özel isimlendirilmiş pipe dosyasını belirtmektedir. 

![image](https://user-images.githubusercontent.com/55113204/109421111-04cecc80-79e7-11eb-81d3-d05d1c22c475.png)

Chmod izinleri harflerle olduğu gibi rakamlar ile de gösterilebilir. r =4, w=2, x=1 değerlerine eşittir. Binary olarak da gösterilebilmektedir. Örneğin 010 okuma yok, yazma var, çalıştırma yok anlamına gelmektedir.
Yetkilendirme izin örneği verecek olursak masaüstü dizininde drwxr-xr-x şeklinde yetkilendirilme verilmiş. Biz burada sadece user tüm yetkilere sahip olsun istiyoruz ve diğerlerinin tüm yetkilerinin kaldırılmasını istiyoruz. Bunun için oluşturmamız gereken komut ‘ chmod u=rwx,go= Masaüstü ’ şeklindedir.

![image](https://user-images.githubusercontent.com/55113204/109421118-0d270780-79e7-11eb-90b2-e831fbaac57d.png)
![image](https://user-images.githubusercontent.com/55113204/109421123-131ce880-79e7-11eb-9d41-376322f647ad.png)

‘*’ parametresi ile dosyaya tüm kullanıcıların okuma erişimi sağlanmaktadır.

# ssh Komutu

Ssh ile bağlantı kurulurken önce kurulacak bilgisayarın rootu (whoami ile bulunuyor) daha sonra ip adresi (ifconfig ile bulunuyor) ssh root@ipadress komutu kullanılarak yazılır. Burada iki makinede ssh açık olmalıdır. Uzaktan bağlantı sağlamak için bağlanmak istediğimiz makinenin password girip connection sağlayabilmekteyiz. 

![image](https://user-images.githubusercontent.com/55113204/109421160-42335a00-79e7-11eb-9fd5-24a2d9fed1e7.png)

# cksum Komutu

Bir dosya veya veri akışı için sağlama toplamı değerini veren komuttur. İlk sayı sağlamada toplam değerdir, ikincisi ne kadar büyüklüğe sahip olduğu ve son kısım ise dosyanın adıdır.

![image](https://user-images.githubusercontent.com/55113204/109421190-5e36fb80-79e7-11eb-9826-c3c9f88f777c.png)

İçerisine bir yazı yazdığımda değeri değişecektir.

![image](https://user-images.githubusercontent.com/55113204/109421201-6727cd00-79e7-11eb-90df-79c816cf71c1.png)

# history Komutu

Daha önce kullandığımız komutları görmek istediğimizde bu komut kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109421422-4ca22380-79e8-11eb-89a7-365dec33b667.png)

History -c ile geçmişi temizleyebilir yada son 5 kullanılmış komutları görüntülemek için history -5 gibi değerler yazılabilir. Grep komutunu kullanarak ise tüm history listelemek yerine istediğimi komutu görüntülemekteyiz. 

![image](https://user-images.githubusercontent.com/55113204/109421428-53c93180-79e8-11eb-9ae3-7d6aa887b72b.png)

Bir komutu tekrar yazıp çalıştırmak yerine history üzerinde işlenmiş sayı numarasına göre “!” ile tekrar komutu çalıştırabiliriz. Misal olarak 74. Satırda cd Masaüstü var ve ben !74 yazarak masaüstüne geçiş yapabildim.

![image](https://user-images.githubusercontent.com/55113204/109421455-6e9ba600-79e8-11eb-9e15-feb64370d693.png)

# cut Komutu

Bu komut bir dosya veya dizinde belirli bir kısmı almak istediğimizde kullanılır. Ilk olarak -c kullanımı görelim. Burada 5. Biti ekrana bastırılır.

![image](https://user-images.githubusercontent.com/55113204/109421470-8115df80-79e8-11eb-9633-07fdcad4cb65.png)

Belirli aralıktaki içerikleri de alabiliyoruz.

![image](https://user-images.githubusercontent.com/55113204/109421478-883ced80-79e8-11eb-9e73-e15a74377ff9.png)

Belirli baytları göstermesi için -b parametresi kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109421501-a60a5280-79e8-11eb-8ce1-16821e4a6399.png)

Satırlardaki istenilen değer kadar kesilip listelenebilir.

![image](https://user-images.githubusercontent.com/55113204/109422046-f7b3dc80-79ea-11eb-86ec-88be86c26797.png)

5. bitten sonrasını görmek istediğimizde de şu şekilde gösterebiliriz.

![image](https://user-images.githubusercontent.com/55113204/109422079-174b0500-79eb-11eb-8417-ee6939d8c5dd.png)

-f parametresi uzunluğu çok fazla olan söz dizilimlerini kesmek için kullanılır.

# date Komutu

Tarih saat bilgisini ayarlamamızı, lokasyon değişikliğine göre güncellememizi yeniden yapılandırmamızı sağlayan komuttur.

![image](https://user-images.githubusercontent.com/55113204/109422093-292ca800-79eb-11eb-9e3b-e806321d6cdf.png)

Zone değişikliğinde lokasyonu setleyebiliriz.

![image](https://user-images.githubusercontent.com/55113204/109422104-334ea680-79eb-11eb-9e09-ce19e607a6f8.png)

# df Komutu

Diskteki boş alanı, ne kadar boş alan olduğunu mount (bağlanma noktasını), doluluğunu, kullanılan alanın boş alana oranı, blok sayısını gösteren komuttur.

![image](https://user-images.githubusercontent.com/55113204/109422130-45304980-79eb-11eb-9c4f-f0aa9262d959.png)

## -a Parametresi

-a paremetresi ile daha ayrıntılı bilgi almaktayız.

![image](https://user-images.githubusercontent.com/55113204/109422135-4cefee00-79eb-11eb-9ba7-27db39bcdb03.png)

## -h Parametresi

Dosyanın boyutu hakkında bilgileri gb cinsinden görmek için -h parametresi,

![image](https://user-images.githubusercontent.com/55113204/109422147-5e38fa80-79eb-11eb-9ae8-661b3ffd98f3.png)

## -i Parametresi

Dosyanın inodesi hakkında bilgilere ulaşmak için -i paremetresi,

![image](https://user-images.githubusercontent.com/55113204/109422154-67c26280-79eb-11eb-82df-a6de0b032fed.png)

## -T Parametresi

Dosyanın tipleri hakkında bilgi edinmek istenilirse -T paremetresi kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109422202-9cceb500-79eb-11eb-83fc-9123d4e61020.png)

## -m Parametresi

Dosyanın mb cinsinden bilgilerine ulaşılmak istenirse -m parametresi kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109422217-ace69480-79eb-11eb-9050-b15ebbc505c8.png)


# fdisk -l Komutu

Sistemdeki diskleri ve bölümlerini listelemek için kullanılan komuttur.

![image](https://user-images.githubusercontent.com/55113204/109422237-c4be1880-79eb-11eb-9bd0-755eea1c4a59.png)

-d parametresi ile disk üzerinde bir bölümü silmek yada biçimlendirmek için kullanılır.
-n parametresi yeni bir disk oluşturur.

# diff Komutu

Difference yani faklılıkları karşılaştıran bir komuttur. -a parametresi ile birlikte kullanıldığında metin dosyası olarak karşılaştırma yapmaktadır.

![image](https://user-images.githubusercontent.com/55113204/109422317-2088a180-79ec-11eb-905b-9767ff0dbadc.png)

6c2 burada 6. Satır ile 2. Satır eşleşmesi için değiştirilmesi gerekiyor.
D ise birinci dosyadaki satır ikinci dosyadaki satırla eşleşecek şekilde silinmelidir. Burada hat 0 sekronize hale gelmesi için ilk dosyadan silinöesi gerek 2 satıra ihtiyaç vardır denilmektedir.

## -r Parametresi

-r parametresi ile varsa alt dizinleri karşılaştırır. 

## -q Parametresi

İki dosyanın birbirinden farklı olduğunu öğrenmek için -q parametresi kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109422384-56c62100-79ec-11eb-822f-37f29dfa0cd8.png)

## -s Parametresi

-s parametresi ile aynı olan dosyaları öğrenmek istediğimiz de kullanırız.

# du Komutu

Du disk kullanımının ne kadar yer kapladığını gösterir. 

![image](https://user-images.githubusercontent.com/55113204/109422417-7b21fd80-79ec-11eb-9f6e-9d7ba204b6ec.png)

## -a Parametresi

-a parametresi içindeki dizinlerin ayrıntılı olarak yer kaplamasını gösterir.

![image](https://user-images.githubusercontent.com/55113204/109422430-85dc9280-79ec-11eb-93b2-81e4a2083ff2.png)

## -c Parametresi

-c parametresi toplam ne kadar disk kullandığını gösterir.

![image](https://user-images.githubusercontent.com/55113204/109422442-912fbe00-79ec-11eb-9a79-eddb368eda9f.png)

## -BG Parametresi

-BG kullanıcıların daha açık bir şekilde anlaması için boyutu gösteren parametredir.

![image](https://user-images.githubusercontent.com/55113204/109422463-ab699c00-79ec-11eb-8843-cec7eabab476.png)

## -ca Parametresi

-ca disk kullanımını ayrıntılı gösteren parametredir.

![image](https://user-images.githubusercontent.com/55113204/109422472-b9b7b800-79ec-11eb-8d91-cfb3ca1e527f.png)

_du -sh .[!.]* * | sort -n parametreleri ile gizli olan dosyaları boyutları ile birlikte göstermektedir._

![image](https://user-images.githubusercontent.com/55113204/109422492-d0f6a580-79ec-11eb-9f16-d8a0395fcc7a.png)

# less Komutu

Bu komut dosyanın içeriğini görüntülememizi sağlamaktadır.
Kullanımı less dosya şeklindedir.

![image](https://user-images.githubusercontent.com/55113204/109422509-e66bcf80-79ec-11eb-8f3b-d944a0dd90fd.png)

# more Komutu

Sayfayı görüntülememizi sağlayan komuttur. Less komutu gibidir.
More -p parametresi ile kullanıldığında önce sayfayı temizler daha sonra görüntüler.

![image](https://user-images.githubusercontent.com/55113204/109422529-f388be80-79ec-11eb-913b-b042ecbd15a4.png)

## -s Parametresi

-s parametresi birden fazla boş satırı tek boş satır olacak şekilde sıkıştırma yapar.

![image](https://user-images.githubusercontent.com/55113204/109422535-ff748080-79ec-11eb-9f8c-e6ec85706802.png)

## -n Parametresi

-n parametresi ile dosyayı satır satır yazar.

## -f Parametresi

-f parametresi ile dosya ismini ve satır numarasını gösterir.

# echo Komutu

Echo ile hangi kabukta olduğunu görmek istiyorsak echo $SHELL komutunu bastırırız.

![image](https://user-images.githubusercontent.com/55113204/109423142-68f58e80-79ef-11eb-8ee3-0e539e385f31.png)

Echo ile ekrana yazı bastırabiliriz.

![image](https://user-images.githubusercontent.com/55113204/109423146-701c9c80-79ef-11eb-9bb2-e4e2c790d7b9.png)

Echo ile yeni bir dosya oluşturabiliriz.

![image](https://user-images.githubusercontent.com/55113204/109423165-8591c680-79ef-11eb-9805-a4dbac0ed88b.png)

Echo ile hem yeni dosya oluşturup hem de içini doldurabiliriz.

![image](https://user-images.githubusercontent.com/55113204/109423173-8b87a780-79ef-11eb-8c79-47a8dc8d7125.png)

Dosyamızı güncelleyebiliriz.

![image](https://user-images.githubusercontent.com/55113204/109423175-92161f00-79ef-11eb-9eb0-37fc5c9ed48c.png)

Echo kullanarak matematiksel işlemleri ekrana bastırabiliriz.

![image](https://user-images.githubusercontent.com/55113204/109423181-99d5c380-79ef-11eb-85ee-703cc73265b4.png)

# locate Komutu

Hızlı olarak arama komutudur. Bir dosyanın nerde olduğunu unuttuğumuzda locate komutu ile dosyanın adını yazarak arama yapmaktayız.

![image](https://user-images.githubusercontent.com/55113204/109425871-8d576800-79fb-11eb-88ba-82335a0844b1.png)
 
 ## -i Parametresi
 
-i parametresi ile kullanıldığında büyük küçük harfleri sorun etmeden arama yapmaktadır.

# wc Komutu

Bu komut sırasıyla satır sayısı, kelime sayısı ve komut sayısını ekrana bastırmaktadır.

![image](https://user-images.githubusercontent.com/55113204/109425877-934d4900-79fb-11eb-8ed6-f5831c3b70b2.png)
 
## -c Parametresi

Karakter sayısını ekrana bastırmak için -c parametresi kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109425882-98aa9380-79fb-11eb-86d9-e5f6ea10aed2.png)
 
## -w Parametresi

Kelime sayısını göstermek için -w parametresi kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109425889-9ea07480-79fb-11eb-9bbd-e1fa43e3eefa.png)

## -l Parametresi

Satır sayısını göstermek için -l parametresi kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109425891-a3652880-79fb-11eb-84c5-2aa3b208246f.png)

# env Komutu

Environment komutu systemin propertiesi hakkında bilgi veren komuttur.

![image](https://user-images.githubusercontent.com/55113204/109425900-a9f3a000-79fb-11eb-8057-f30c29496b98.png)

# expand Komutu

Girdi de verilen tab değerini space değerine çevirme işlemi yapmaktadır.

![image](https://user-images.githubusercontent.com/55113204/109425907-aeb85400-79fb-11eb-8275-bd4b80865462.png)

# free Komutu

Bir işletim sisteminde belleğin ne kadarının kullanıldığı ve ne kadarının boş olduğunu göstermeye yarayan komuttur.

## -h Parametresi

-h parametresi kullanarak çıktımızı daha anlamlı hale çevirebiliriz.

![image](https://user-images.githubusercontent.com/55113204/109425911-b5df6200-79fb-11eb-936b-c5c934d58b38.png)

Burada takas ve memory kullanımını görebilmekteyiz. Ne kadarının paylaşıldığını ne kadarının meşgul olduğunu total de ne kadarlık belleğe sahip olduğumuzu görmekteyiz.

# ps Komutu

Ps komutu o anda çalışan işlemleri gösteren komuttur.

## -A Parametresi

-A parametresi kullanarak çalışan tüm işlemler gösterilmektedir.

![image](https://user-images.githubusercontent.com/55113204/109425975-18386280-79fc-11eb-97f6-549a8e7ad866.png)

## -ax Parametresi

-ax parametresi kullanılarak o anda çalıştırabilir tüm işlemler gösterilmektedir.

![image](https://user-images.githubusercontent.com/55113204/109425979-1c648000-79fc-11eb-94bf-d8934ca0192f.png)

## -aux Parametresi

Ps aux parametresi kullanılarak daha simple şekilde gösterilmektedir.

![image](https://user-images.githubusercontent.com/55113204/109425983-24242480-79fc-11eb-8cdc-f58a6c9d34a7.png)
 
## -L [istenilen_satır] Parametresi

Bu parametre ile istenilen satır hakkında detaylı bilgi edinilmektedir.

![image](https://user-images.githubusercontent.com/55113204/109425988-2a1a0580-79fc-11eb-8776-327b47444a68.png)

## -C Parametresi

-C bash parametresi çalıştırılan bash işlemleri hakkında bilgi vermektedir.

![image](https://user-images.githubusercontent.com/55113204/109425995-2e462300-79fc-11eb-9e84-3f2c94b92acc.png)

## -U root -u root Parametresi
 
Çalıştırılmış root işlemleri hakkında bilgi almak istediğimizde -U root -u root parametresini kullanmaktayız.

![image](https://user-images.githubusercontent.com/55113204/109425997-32724080-79fc-11eb-8210-cd3dd9fa4790.png)

## -e Parametresi
 
-e parametresi sistemde çalışan her süreç hakkında bilgi verir. 

## -u Parametresi

-u kullanıcı adına göre süreç bilgilerini verir.

## -p Parametresi

-p süreç numaralarına göre (PID) süreç bilgisi verir.


# pstree Komutu 

Süreci hiyerarşik olarak görüntülemek istersek bu komutu kullanırız. Bir ağaç gibi bize ayrıntılı anlatmaktadır. 
 
 ![image](https://user-images.githubusercontent.com/55113204/109426000-3b631200-79fc-11eb-95fe-876592d1ba05.png)

# top Komutu

Bu süreci 3 saniyede bir yenilerek sistemin anlık sürecini bilgi verir. -d saniye parametresi şeklinde yazarak anlık güncellenen süreyi değiştirebiliriz. Q ile çıkış yaparız.

![image](https://user-images.githubusercontent.com/55113204/109426004-3f8f2f80-79fc-11eb-86e4-ffe5fa7c19be.png)

# head Komutu

Head komutu listelenmiş dosyada default olarak ilk 10 komutu vermektedir. Biz istersek -n [değer]parametresi ile görmek istediğimiz kadar değeri listeleyebiliriz.

![image](https://user-images.githubusercontent.com/55113204/109426386-94cc4080-79fe-11eb-93dc-e5ee4e79e7d6.png)

# tail Komutu 

Default olarak sondan 10 tane girdiyi bize çıktı olarak vermektedir. -n [değer] parametresi ile kaç değerin listelenmesini istersek çıktı olarak alabiliriz.

![image](https://user-images.githubusercontent.com/55113204/109426391-9ac22180-79fe-11eb-8129-6e5cde87b86c.png)

# hostname 

Hostname hakkında bilgi edinmek istenirse

![image](https://user-images.githubusercontent.com/55113204/109426402-a877a700-79fe-11eb-87eb-c784eeb2e407.png)

Başka bir alternative olarak şu şekilde de hostname öğrenebiliriz.
 
![image](https://user-images.githubusercontent.com/55113204/109426408-b4636900-79fe-11eb-8d6e-de6e40f0c24e.png)

# wget Komutu

Dosya indirme komutudur. Indirmek istenilen dosyanın url/dosyaadı şeklinde yazarak indirebiliriz.

![image](https://user-images.githubusercontent.com/55113204/109426412-b7f6f000-79fe-11eb-9d9f-826f41d4518d.png)

# curl Komutu

Veri transferi sağlayan ve url ile verilerin bağlanılımını kontrol ettiğimiz komuttur.

![image](https://user-images.githubusercontent.com/55113204/109426419-bd543a80-79fe-11eb-9623-756480b987d1.png)

## -C - Parametresi

-C - parametresi ile kesilen indirmeyi devam ettirmemiz sağlanır.
Iki dosyanın indirim işlemi yapmak istediğimizde iki url kullarak kaydetmek istediğimiz alanı da belirterek uygulayabiliriz.

![image](https://user-images.githubusercontent.com/55113204/109426428-c218ee80-79fe-11eb-8db8-0981fa0c92f7.png)

# -I Parametresi 

Bir web sitenin HTTP başlıklarını sorgulamak için -I parametresi kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109426545-4d927f80-79ff-11eb-8d2d-1cb615db8323.png)

## curl ile bir domainin get isteğini alma

![image](https://user-images.githubusercontent.com/55113204/109426548-52efca00-79ff-11eb-8960-6951488b9c44.png)
 
Bir web sitesine girdiğimizde hangi cookielerin indirildiğini görmek için bunu bir dosyaya kaydedip görüntüleyebiliriz.

![image](https://user-images.githubusercontent.com/55113204/109426550-57b47e00-79ff-11eb-93f8-48136ed70b9e.png)
 
## curl ile sunucuya bir post isteği atma

![image](https://user-images.githubusercontent.com/55113204/109426563-60a54f80-79ff-11eb-8d7a-b980478a1983.png)
 
# id Komutu

Kullanıcının id bilgilerini veren komuttur.
 
![image](https://user-images.githubusercontent.com/55113204/109426568-656a0380-79ff-11eb-8e1d-7e325223454d.png)

 ## -g Parametresi 
 
-g parametresi ile etkili kullanıcın id numarası bastırılır.

![image](https://user-images.githubusercontent.com/55113204/109426570-6b5fe480-79ff-11eb-877e-bf1c455a063c.png)

# passwd Komutu

Password değişimi yapmak için kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109426574-70249880-79ff-11eb-90c7-6260a5aed5ef.png)

# kill Komutu

Cevap vermeyen processleri sinyaller ile öldürmek için kill komutu kullanılır. Pid ile birlikte kullanılır. Burada PID değerini bulup kill -l ile nasıl bir kill kullanacağımızı belirlemeliyiz.

![image](https://user-images.githubusercontent.com/55113204/109426582-7c105a80-79ff-11eb-9706-1df7f98afa18.png)

# killal Komutu

Bu komut tüm ilişkili sistemi öldürmemizi sağlayan komuttur.
Killal -9 apache örnek verilebilir.

# man Komutu
Bir konu hakkında detaylı bilgi almak istenildiğinde man komutu kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109426583-816da500-79ff-11eb-8739-5ff7f396da27.png)
 
# rm Komutu
Rm komutu bir dosya yada dizin silmek için kullanılan komuttur.

![image](https://user-images.githubusercontent.com/55113204/109426591-8af70d00-79ff-11eb-8b84-684c27823cac.png)

## -i Parametresi 

Onay isteyerek silmesini -i parametresi kullanılmaktadır. 

## -r Parametresi 

Alt dizin yada dosyaların silinmesini -r parametresi sağlamaktadır. 

## -v Parametresi 
Yapıalan silmeyle ilgili bilgilerin elde edilmesi için de -v parametresi kullanılmaktadır.

# watch Komutu

Saat hakkında bilgi veren komuttur.

![image](https://user-images.githubusercontent.com/55113204/109426607-964a3880-79ff-11eb-8a5d-088564e13549.png)

# sort Komutu

Harf yada ilk bit sıralamasına göre dizen bir sıralama komutudur.

![image](https://user-images.githubusercontent.com/55113204/109426612-9b0eec80-79ff-11eb-8a35-43d99af43be1.png)

## -r Parametresi 

Tersten sıralama yapılmasını istiyorsak -r parametresi kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109426623-a6621800-79ff-11eb-924e-df846ec18a33.png)
 
# uname Komutu

Makine hakkında bilgiler verir. Ilk olarak kullanılan kernel adını(linux), bilgisayarın ağ üzerindeki host adını(kali), kernel ana dağıtım bilgisini (5.5.0-kali2-amd64), yayınlandığı tarihle birlikte kernelin dağıtıma özel sürüm bilgisi, kullanılan bilgisayarın donanım adı ve kullanılan işletim sisteminin adı sırasıyla verilmektedir.

![image](https://user-images.githubusercontent.com/55113204/109426651-c1348c80-79ff-11eb-9f4a-5911e3d68ee7.png)

# split Komutu

Boyutu çok büyük olan dosyaların daha küçük boyuttaki dosyalara bölünmesi için split komutu kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109426659-d4475c80-79ff-11eb-9edb-4dc18dad23a2.png)

## wc -l * Parametresi

Burada 13 satırlık funda2 dosyasını 5 satır şeklinde bölerek part1 isminin türevleri olan dosyalara atadım. Bu dosyaları wc -l * parametresi ile görüntülecek olursak şeklinde çıktı alırız.

![image](https://user-images.githubusercontent.com/55113204/109426763-52a3fe80-7a00-11eb-8c72-cfa7181e5c12.png)

# tee Komutu

Dosyalara standart girdiği ve çıktıyı kopyalan komuta denir.

## -a Parametresi

Listelediğimiz standart çıktı logunu birbirinin üzerine yazıp eski dosyayı silmesin diye -a parametresi ile filtrelemekteyiz.

![image](https://user-images.githubusercontent.com/55113204/109426770-5cc5fd00-7a00-11eb-8dd4-b4157a0b9a22.png)

## Birden fazla log dosyası oluşturmak için

Birden fazla log dosyası oluşturmak için de ls | tee file1 file2 … şeklinde yazabiliriz.

# uptime Komutu

Sistemin ne kadar süredir aktif olarak çalıştığını gösteren komuttur. Geçerli zaman, çalışma süresi, kullanıcı sayısı, ortalama yük olarak sıralanmaktadır.

![image](https://user-images.githubusercontent.com/55113204/109426781-694a5580-7a00-11eb-94fb-e09d2da2b248.png)

# find Komutu

Bulmak istediğimiz dosyarı find komutu ile erişebiliriz. 

![image](https://user-images.githubusercontent.com/55113204/109426788-70716380-7a00-11eb-8d61-70bd12b45b6a.png)

Içinde bazı kelimelerin geçtiği dosyaları arıyorsak *dosya_adı şeklinde arama yapabiliriz.
Root yetkisi vererek gizli olan dosyalar da dahil arama yapmak istiyorsak sudo su sadece tek bir defalık root yetkisine sahip olmak istiyorsak sudo araması yapabiliriz.

![image](https://user-images.githubusercontent.com/55113204/109426792-76ffdb00-7a00-11eb-8905-1008b01f8114.png)

Root olarak txt tipinde arama yapmak istediğimizde kullanılan komut sudo find / -name  “*txt”

![image](https://user-images.githubusercontent.com/55113204/109427010-7156c500-7a01-11eb-9513-eb13eb52bea8.png)

## -i Parametresi 

Büyük küçük harflere karşı duyarsız olmasını istiyorsak -iname parametresi kullanılmaktadır.
Belirli bir dizinde arama yapmak istenildiğinde ise;

![image](https://user-images.githubusercontent.com/55113204/109427028-892e4900-7a01-11eb-8ed8-97dde6e0c548.png)

Belgeler dizinin altında .txt uzantılı dosyaları fundaeren.png adında bir dosya oluşturacak ve içerisine sıkıştıracaktır.

![image](https://user-images.githubusercontent.com/55113204/109427033-90eded80-7a01-11eb-9cf8-54fefad061ae.png)

Belgelerdeki 10M altındaki dosyaları listelemektedir.

![image](https://user-images.githubusercontent.com/55113204/109427036-964b3800-7a01-11eb-9097-3114d1aaade3.png)

Gizli olan dosyaları görmek için find / home -type f -name “.*” komutu kullanılır.
Bir kullanıcı arıyorsak find / -type f -user isim -name “.log.txt”
Son 2 gün içinde değiştirilmiş dosyaları arıyorsak find / -type f -mtime 2
1-7 gün arasındaki değişiklikleri görmek istiyorsak find / -type f -mtime +1 -mtime -7
30 dk içinde değiştirilmiş dosyaları görmek istediğimizde find / -type f -cmin -30 parametreleri kullanılır.

# scp Komutu 

Cp gibi kopyalama komutu olduğunu düşünebiliriz. Kopyalayacağımız dosyayı nereye kopyalayacağımızı gösteren komuttur.

![image](https://user-images.githubusercontent.com/55113204/109427054-a82cdb00-7a01-11eb-85e6-13aad74119e4.png)

Eğer kendi bilgisayarımızdan başka bilgisayara dosya kopyalamak istiyorsak
Scp dosya user@host:Nereye_kopyalanacak?

![image](https://user-images.githubusercontent.com/55113204/109427065-b1b64300-7a01-11eb-858f-59b28a98d81d.png)

Karşı bilgisayardan kendi bilgisayarımıza dosya kopyalamak için gerekli olan komut

Scp user@host:dosya_adı nereye_kopyalanacağı?

![image](https://user-images.githubusercontent.com/55113204/109427106-da3e3d00-7a01-11eb-9001-8214b79b131a.png)

# grep Komutu

Find komutu gibi arama yapmak için kullanılır. Dosya içinde u harfi olanları ekrana bastırmaktayız. 

![image](https://user-images.githubusercontent.com/55113204/109427114-e6c29580-7a01-11eb-9f1f-dfbd59038760.png)

Büyük küçük harfe duyarlıdır bundan dolayı U araması yaptığımızda sonuç vermeyecektir.

![image](https://user-images.githubusercontent.com/55113204/109427130-f80ba200-7a01-11eb-92f3-c794515c8b7a.png)

## -I Parametresi

Büyük küçük harf duyarlılığını kaldırmak için -I parametresi kullanılmalıdır.

![image](https://user-images.githubusercontent.com/55113204/109427164-27baaa00-7a02-11eb-8a93-09b9c24bf4c2.png)

## -v Parametresi

Bazı kelimeler dışında arama yapmak istediğimizde -v parametresi kullanarak arama yapabiliriz. Burada u harfi içeren satırlar gelmesin istedik.

![image](https://user-images.githubusercontent.com/55113204/109427172-2d17f480-7a02-11eb-8836-ee93a5a95c96.png)

## -r Parametresi

Dizindeki tüm dosyalarda arama yapılmasını istiyorsak -r parametresi kullanmaktayız.

![image](https://user-images.githubusercontent.com/55113204/109427191-4456e200-7a02-11eb-83e2-d1c4aa98b0c8.png)

## -n Parametresi 

Satır numarası kullanarak çıktı almak istediğimizde kullanmamı gereken parametre -n dir.

![image](https://user-images.githubusercontent.com/55113204/109427201-50db3a80-7a02-11eb-88a8-d35b2e1d8a6c.png)

# chown Komutu

Bu komut kulanıcı değiştirmektedir. Sudo olarak yetkiyi devretmekteyiz. 

Sudo chown user dosya şeklinde yazılan komut sıralamasıdır. 

Bir dosyanın kulllanıcısını değiştirebiliriz. Burada funda kullanıcılı bir dosyayı fatma kullanıcısının dosyası olarak değiştirdik.  Ls -l komutu ile değişip değişmediğini görüntüledik.

![image](https://user-images.githubusercontent.com/55113204/109976552-f3e6c980-7d0c-11eb-8208-5584b59b55fa.png)

![image](https://user-images.githubusercontent.com/55113204/109976569-f77a5080-7d0c-11eb-8efc-e1d944fa3705.png)

Aynı şekilde grup bilgisi de değiştirilebilir. Grubu funda olan fatma kullanıcılı dosyanın grubunda fatma olarak değiştirebiliriz.

![image](https://user-images.githubusercontent.com/55113204/109976598-019c4f00-7d0d-11eb-8b3b-dc736ea477fb.png)

![image](https://user-images.githubusercontent.com/55113204/109976616-04973f80-7d0d-11eb-8e24-5b7fce3acc2c.png)

Kullanıcıyı değiştirmeden sadece grubu da değiştirebiliriz. Biz burada kullanıcısı ve grubu funda olan deneme ismindeki dosyayı kullanıcısını değiştirmeden grubunu fatma yaptık.

![image](https://user-images.githubusercontent.com/55113204/109976641-0d881100-7d0d-11eb-836b-db071b1a7769.png)

![image](https://user-images.githubusercontent.com/55113204/109976650-11b42e80-7d0d-11eb-8158-176ddce62ef3.png)

Dizinlerinde kullanıcılarını değiştirebilmekteyiz. Kullanıcısı funda olan bir dizinin kullanıcısını fatma olarak değiştirdik.

![image](https://user-images.githubusercontent.com/55113204/109976673-1973d300-7d0d-11eb-9aff-404d7baa0d15.png)

![image](https://user-images.githubusercontent.com/55113204/109976688-1ed11d80-7d0d-11eb-9ccb-1d37de552abf.png)

Sadece grubu da değiştirebiliriz. Grubu funda olan bir dizinin grubunu fatma olarak değiştirdik.

![image](https://user-images.githubusercontent.com/55113204/109976719-27295880-7d0d-11eb-8b05-945c526b71e2.png)

![image](https://user-images.githubusercontent.com/55113204/109976740-2c86a300-7d0d-11eb-9b83-ae277e9d5d06.png)

![image](https://user-images.githubusercontent.com/55113204/109976756-301a2a00-7d0d-11eb-8c2f-490d682760b7.png)

Hem kullanıcıyı hemde grubu değiştirebiliyoruz.

![image](https://user-images.githubusercontent.com/55113204/109976790-37d9ce80-7d0d-11eb-99fb-529409d4879d.png)

![image](https://user-images.githubusercontent.com/55113204/109976811-3b6d5580-7d0d-11eb-9dad-5d0283210f8c.png)

![image](https://user-images.githubusercontent.com/55113204/109976828-3f997300-7d0d-11eb-85b3-194f3b97594f.png)

Sembolik bir bağlantı mevcut bir fiziksel dosyaya referans olan linklere soft link denmektedir. Biz burada soft linkte oluşturabiliriz.

![image](https://user-images.githubusercontent.com/55113204/109976872-488a4480-7d0d-11eb-8141-08f17178bcc6.png)

![image](https://user-images.githubusercontent.com/55113204/109976889-4b853500-7d0d-11eb-895f-634a927402cb.png)

Sembolik linkte kullanıcıyı değiştirsek fiziksel dosyanın da kullanıcısı değişmektedir. Burada sembolik linkin değil fiziksel dosyanın sahipliğini değiştirdik.

![image](https://user-images.githubusercontent.com/55113204/109976918-5344d980-7d0d-11eb-877c-bcc314dc5602.png)

![image](https://user-images.githubusercontent.com/55113204/109976934-563fca00-7d0d-11eb-996e-67911de64c87.png)

![image](https://user-images.githubusercontent.com/55113204/109976948-59d35100-7d0d-11eb-9e9a-6119ec71a07d.png)

Eğer sembolik linkinde sahipliğini değiştirmek istersek şu şekilde olur.

![image](https://user-images.githubusercontent.com/55113204/109976978-62c42280-7d0d-11eb-860b-cf86cd398571.png)

![image](https://user-images.githubusercontent.com/55113204/109976991-6657a980-7d0d-11eb-8a10-3920920516d2.png)

![image](https://user-images.githubusercontent.com/55113204/109976999-68ba0380-7d0d-11eb-8738-d990ae768a9c.png)

-R parametresi ile de tüm dizin ve alt dizinlerin sahipliğini ve grubunu kesin olarak değiştirebiliriz.


# awk Komutu

Awk programlama dili yazılımsal olarak ifade filtrelemektir. Burada -F alanı ayırmaya yarayan parametredir. Yani noktalı virgüle ayrılmış kısmı ayırmaktadır. $ ile belirtilen kısım hangi indeksleri istiyorsak o indeksleri bize verip ekrana bastırmaktadır. Biz burada 2. indeksteki değeri ekrana bastırmak istedik. 

![image](https://user-images.githubusercontent.com/55113204/109427221-6b151880-7a02-11eb-8e9b-ffa3f33e638b.png)

Data.txt veri akışındaki veriyi 2. indeksteki değeri alır ve ekrana bastırır.

![image](https://user-images.githubusercontent.com/55113204/109427227-6fd9cc80-7a02-11eb-9f39-415aab865d61.png)

3. indekste bulunan değerlerin toplam değerini ekrana bastırır.

![image](https://user-images.githubusercontent.com/55113204/109427231-749e8080-7a02-11eb-80df-59010fd26fcd.png)
 
2. ve 5. Indeksler arasındaki değerleri ekrana bastırır.

![image](https://user-images.githubusercontent.com/55113204/109427235-7b2cf800-7a02-11eb-828f-aef4bf16dd1c.png)

# sed Komutu

Sed komutu bu komutu kullanarak dosyaların içinde değişiklikler yapabilmekteyiz. burada ; ile ayrılan kısımı , ile ayırma işlemi yaptık.

![image](https://user-images.githubusercontent.com/55113204/109427247-8da73180-7a02-11eb-8098-47aa0886ace0.png)

Istediğimiz satırı belirlediğimiz koşullarda silebiliriz. Biz burada I harfi ile başlayan satırları sildik.

![image](https://user-images.githubusercontent.com/55113204/109427255-9435a900-7a02-11eb-8826-48d85b30d9a1.png)

Sildiğimiz satırları geri getirebilriz.

![image](https://user-images.githubusercontent.com/55113204/109427267-9bf54d80-7a02-11eb-98d2-30572faf09ac.png)
 
Belirli bir indisteki satırı silebiliriz biz burada 2. Satırı sildik.

![image](https://user-images.githubusercontent.com/55113204/109427273-a1529800-7a02-11eb-979a-1cd9042bef65.png)

Belirli aralıktaki ifadeleri ekrana bastırabiliriz. Burada ise 1 ve 5. Satırlar arasındaki ifadeleri ekrana bastırmak istedik.
 
 ![image](https://user-images.githubusercontent.com/55113204/109427276-a6afe280-7a02-11eb-9847-0e02ba43cb59.png)

# axel Komutu

Dosya indirmeyi sağlayan komuttur. Axeli öncelikle sistemimize kurup daha sonra istenilen dosyanın link adresi verilmelidir.

![image](https://user-images.githubusercontent.com/55113204/109427283-add6f080-7a02-11eb-88ad-1ed6365a501a.png)

# netcad Komutu

nc komutu ağ trafiğini dinleme yapmaktadır. Burada google.com 80 portu üzerinden dinleme yaptık.

![image](https://user-images.githubusercontent.com/55113204/109427291-b7f8ef00-7a02-11eb-88a2-4aed8200bfd1.png)

## -nv Parametresi

Hangi portların açık yada kapalı olduğunu öğrenmek için -nv parametresini kullanırız.

![image](https://user-images.githubusercontent.com/55113204/109427296-bb8c7600-7a02-11eb-8b10-bd2cca74f779.png)

## -nvlp Parametresi 

Dosya aktarımında kullanılan parametre -nvlp parametresi kullanılır. Biz burada web sitemize 443 porttan bağlandık.

![image](https://user-images.githubusercontent.com/55113204/109427298-c0512a00-7a02-11eb-9ce1-0504673e7993.png)

# exiftool Komutu

Bu komut bir resim dosyası hakkında ayrıntılı bilgi vermektedir.

![image](https://user-images.githubusercontent.com/55113204/109427301-ca732880-7a02-11eb-8264-3ea77fd63c1d.png)

# socat Komutu

Zayıf güvenlik duvarlarına saldırmak için Tcp bağlantı noktası ileticisini çift yönlü bayt akışı oluşturarak kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109427305-cfd07300-7a02-11eb-8b00-2c3e560e2cd7.png)



# LİNUX DOSYA SİSTEM HİYERARŞİSİ NEDİR?

Dosy Sistem Hiyerarşisi linux bir kök dizin yapısına sahiptir. Öncelikle root olan kök dizinden sırasıyla alt dizinlere doğru ayrılır. Bu ayrılma / ile gösterilmektedir. Kök dizinimiz bizi en yetkili kullanıcımız anlamına gelmektedir. Onun sistemde yaptığı değişiklikler yetkili olduğu için bir soruna sebep olmamaktadır. Sistemde bir dizin yada dosyada kalıcı değişiklikler yapılması için yetki yükseltilmesi yapılıp root olunması gerekmektedir. Alt dizinlere yarılan linux dağıtık bir sistemdir. Dağıtık sistem tek bir makinede tüm özelliklerin bulunmamasıdır. Ağ üzerinden iletişim halinde olan bir çok makine farklı sunucuları farklı makinelere kullanıp ağ üzerinden iletişime geçebilir. Bu şekilde tek bir makinenin yükü azalarak performansı artmaktadır.

## /bin dizini

Temel komutlar bu dizinde çalışmaktadır. Sistemde herhangi bir sorun olduğunda bin dizini çalışmaya devam etmektedir. Komutlar çalışmaya devam ettiğinden dolayı sistemdeki sorun /bin dizini sayesinde düzelebilmektedir.

![image](https://user-images.githubusercontent.com/55113204/109977832-470d4c00-7d0e-11eb-8ae8-3d99e03627a0.png)

## /boot

Sistemi boot etmek işletim sitemine ulaşarak bilgisayar açılırken öncelik verdiğimiz sistemin yüklenerek sisteme güç vermesi demektir. Sistemin boot öncelik ayarlarını değiştirebilmek için BIOS a girmemiz gerekir. BIOS donanım çalışırken işletim sistemi ile aradaki iletişimi kuran yazılım işletim sisteminin nereden yükleneceğini bileni donanımsal protokolleri belirleyen ve işletim sisteminin öncelikle hangi donanımı okumasını sağlayan yazılımdır.

![image](https://user-images.githubusercontent.com/55113204/109978118-981d4000-7d0e-11eb-990f-8ed7cfc5cdb9.png)

## /dev

Linuxtaki herşey dosya şeklinde dizinlere ayrılmıştır bunların içine donanım aygıtları olan fare, modem gibi aygıtların bağlandığı portlar olan tty dizini, birincil ses kayıtlarının olduğu dsp aygıtlarını içerir.

![image](https://user-images.githubusercontent.com/55113204/109978141-9d7a8a80-7d0e-11eb-8769-35b11f590d93.png)

## /etc

Sisteme dair tüm yapılandırmaları ve bilgisayara özel yapılandırmaları içermektedir. Çalıştırılabilir dosyalar bulunmamaktadır. 

![image](https://user-images.githubusercontent.com/55113204/109978161-a4a19880-7d0e-11eb-945c-700ca3777e41.png)

## /home

Kişisel verilerinin depolandığı, başka programlara yaptığı değişiklikler burada depolanmaktadır. Ayrıca kullanıcının resim, müzik gibi dosyaları da burada tutulmaktadır.
 
![image](https://user-images.githubusercontent.com/55113204/109978190-ac613d00-7d0e-11eb-8832-bf02dcf182cd.png)

## /initrd

Çekirdek yüklenmesinden sonra oluşan bellek diskin üzerinde root olarak açılmasını sağlamaktadır.

## /lib

Çekirdeğe ai tolan modüller ve kütüphane dosyaları burada tutulmaktadır.

![image](https://user-images.githubusercontent.com/55113204/109978208-b2571e00-7d0e-11eb-832b-b9fdfdb33d1e.png)

## /mnt

Sabit disk ve tüm donanımsal aygıtların bağlanma noktasır. İşletim sisteminin kurulu olduğu disk buna değildir.
## /opt

İşletim sisteminden bağımsız, kurulumu zorunlu olmayan programların bulunduğu dizindir.

## /proc

Fiziksel dosyaların bulundurulmadığı donanımsal yapılandırmalar, süreç, bağlı aygıtların bulunduğu sanal bir dosya sistemidir.

![image](https://user-images.githubusercontent.com/55113204/109978247-bd11b300-7d0e-11eb-8f6e-e79a56acd4ea.png)

## /root

Yetkilendirme olarak en üst yetkiye sahip olan kulllanıcıdır. Sistemdeki tüm değişikliklere izini bulunmaktadır. Kullanıcı olarak yapılamayacak tüm işlemleri root olarak yapılandırılabilir. Kalıcı olarak root olmamıza sistem izin vermemektedir. Geçici olarak root olma yetkisi için sudo komutu kullanılır ve sistem root olmanız için makinenin parolasını istemektedir.

## /sbin

Root tarafında kullanılacak yönetimsel ve bakımsal programlar bu dizin altında tutulmaktadır. Genellikle sistem yöneticisi tarafından kullanılmaktadır.

![image](https://user-images.githubusercontent.com/55113204/109978271-c3a02a80-7d0e-11eb-904f-541e5cc0da79.png)

## /user

Sadece kullanılan makineye özel local klasör olan usr komutlar, programlar, kütüphaneler gibi tüm kullanıcılara paylaşılan verileri içeren dizindir.

## /var

Sisteme ait güvenlik duvarını ve sisteme düşen logları görüntülemek için ve e-posta, yazıcı kuyrukları bu dizin altında tutulmaktadır.

## /tmp 

![image](https://user-images.githubusercontent.com/55113204/109978288-c864de80-7d0e-11eb-8f4b-4e63788a623e.png)

Geçici programların depolandığı dizindir. Belirli zaman aralıklarında temizlendiğinden dolayı önemli programları buraya kurmamalısınız. Çünkü makine yeniden başlatıldığında silinir. 



# DİZİN İŞLEMLERİ

# pwd Komutu

Ben neredeyim? Bunu öğrenmek için kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109427724-c0522980-7a04-11eb-881b-6151372927d8.png)

# cd Komutu 

Bir dizine girilmek istendiğinde kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109427726-c47e4700-7a04-11eb-9fb7-64e5ab55defe.png)

Cd .. o dizinden çıkılmak istendiğinde kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109427728-c8aa6480-7a04-11eb-8ed6-ecbc26ddc03b.png)

Cd – ile bir önceki bulunduğumuz dizine döneriz.

![image](https://user-images.githubusercontent.com/55113204/109427734-cd6f1880-7a04-11eb-9581-915fecb8c906.png)
 
Cd - - en başa döneriz.

![image](https://user-images.githubusercontent.com/55113204/109427742-d2cc6300-7a04-11eb-8d18-be41f5742d03.png)

Herhangi bir parametre kullanacak olursak kullanılan komuttan sonra -parametre şeklinde bir dizilim yaparız.

# Full Path 

/ kullanarak çalışma dizine bağlı olmadan istediğimiz yere gidebilmemizi sağlayan araçtır.

![image](https://user-images.githubusercontent.com/55113204/109427751-dcee6180-7a04-11eb-92b9-775b03c41890.png)

# Relative Path

Nerede olduğumuza bağlı olarak yolumuzu belirterek istediğimiz yere o güzergahta gidebildiğimiz araçtır.
 
![image](https://user-images.githubusercontent.com/55113204/109427757-e677c980-7a04-11eb-8f68-16975675e955.png)

O komutlar hakkında daha fazla bilgi edinmek için man, help ve info komutları kullanılmaktadır.
Man ile ls komutu hakkında bilgi edinelim

# Komut man help

![image](https://user-images.githubusercontent.com/55113204/109427777-fee7e400-7a04-11eb-9ed8-cfa69f2e4970.png)
 
Help komutu ile ls hakkında bilgi edinelim. 

![image](https://user-images.githubusercontent.com/55113204/109427781-03ac9800-7a05-11eb-83a6-996dadea08da.png)
 
Info kumutu ile bilgi edinme

![image](https://user-images.githubusercontent.com/55113204/109427785-0909e280-7a05-11eb-97ab-33f4e4497586.png)

# mkdir Komutu

Dizin oluşturmak için kullanılır. 

![image](https://user-images.githubusercontent.com/55113204/109427789-10c98700-7a05-11eb-9678-33be3647ae65.png)

Alt dizinlerde aynı anda oluşturulabilir.

![image](https://user-images.githubusercontent.com/55113204/109427791-158e3b00-7a05-11eb-97ba-b086e4bfb3e5.png)

# rmdir Komutu

İçi boş dizinleri silmek için rm komutu kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109427794-1c1cb280-7a05-11eb-9e9d-182f0d50e6bf.png)

# rm Komutu

İçi dolu dosyaları silmek için rm, dizinleri silmek için rm -r komutu kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109427801-22ab2a00-7a05-11eb-8cf9-1cfd0f46bea9.png)

## -i Parametresi

-i parametresi silinsin mi silinmesin mi onu sorgular.

![image](https://user-images.githubusercontent.com/55113204/109427809-2a6ace80-7a05-11eb-8861-5cdf6e0c3570.png)

## -f Parametresi

-f parametresi sormadan siler

## -r Parametresi

-r parametresi bulunduğu dizinin alt dizinlerini de siler.

## -v Parametresi

-v parametresi ne yapıldığı bilgisini alt kullanıcıya da döndürür. 

![image](https://user-images.githubusercontent.com/55113204/109427813-30f94600-7a05-11eb-9d1e-cc1c7ff58a16.png)

# ln Komutu

Dosyalara link yapmak için kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109427820-35bdfa00-7a05-11eb-8fb5-049328030044.png)

![image](https://user-images.githubusercontent.com/55113204/109427839-3e163500-7a05-11eb-8fbc-f003d04e0075.png)

![image](https://user-images.githubusercontent.com/55113204/109427843-41112580-7a05-11eb-874b-d6766c7f283c.png)
  
# file Komutu

Dosya mı dizin mi ne olduğunu bilmediğimiz zaman bu komutu kullanarak öğrenebiliriz.

![image](https://user-images.githubusercontent.com/55113204/109427850-49696080-7a05-11eb-8d2e-32a3a6bb47e4.png)

‘>’ önüne 1 yazılır yada yazılmaz ise standart çıkışı ekrana verir. 2 yazılırsa komut çalışırken alınan hatalar dosyaya yönlendirilir. Yönlendirmede kullanılan tek ‘>’ eğer yönlendirilecek dosya yoksa dosya oluşturulur varsa dosya içi temizlenir ve çıktıyı yönlendirmektedir.
Yönlendirmedeki yönlendirme işaretinin çift olması “>>”,eğer yönlendirilecek dosya yok ise oluşturulur, dosya var ise çıktıyı dosyanın sonuna yönlendirir.

‘^’  Satır başını belirtir.
‘$’ Satır sonlarını belirtir.
‘.’ Sadece bir karakter ile eşleşir,bir karakter ifade eder
‘*’ Kendinden önceki karakterden 0 veya daha fazla olmasını belirtir
‘[]’ Köşeli Parantez içindeki karakterlerden sadece biriyle eşleşir.
‘[^]’ Köşeli parantez içinde olmayan karakterlerle eşleşir.
+ Kendinden önceki karakter en az 1 veya daha fazla karakteri ifade eder.



# KULLANICI İŞLEMLERİ

Kullanıcı değiştirme için su komutu kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109428279-7880d180-7a07-11eb-850d-0e2121cf78e9.png)

Root olmak için sudo komutu kullanılır.
Yeni kullanıcı ekleme için sudo adduser name dizilimi kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109428283-7cacef00-7a07-11eb-9736-93634101cda9.png)

Kullanıcı şifresini değiştirmek için passwd parametresi kullanılır.

![image](https://user-images.githubusercontent.com/55113204/109428286-8171a300-7a07-11eb-852a-858365612785.png)

## Kullanıcı silme

![image](https://user-images.githubusercontent.com/55113204/109428293-89314780-7a07-11eb-9a0f-97261ba10239.png)
 
-r parametresi ile kullanıcıya ait her şeyi sileriz.

## Grup oluşturma

![image](https://user-images.githubusercontent.com/55113204/109428297-90f0ec00-7a07-11eb-9fdc-b89dab35c050.png)
 
## Grup silme
 
![image](https://user-images.githubusercontent.com/55113204/109428300-964e3680-7a07-11eb-8793-cbebdee6aaf4.png)

## Kullanıcının üye olduğu grupları gösterme

![image](https://user-images.githubusercontent.com/55113204/109428305-9a7a5400-7a07-11eb-9b6d-8f3cdce388ac.png)

## Kullanıcıyı yetkilendirme

![image](https://user-images.githubusercontent.com/55113204/109428310-a0703500-7a07-11eb-89bd-4fe72f4c2cdc.png)

## Kullanıcıyı kilitleme

![image](https://user-images.githubusercontent.com/55113204/109428311-a49c5280-7a07-11eb-9fe9-05e5b50c9b7f.png)

## Kullanıcının kilidini kaldırma

![image](https://user-images.githubusercontent.com/55113204/109428315-a9610680-7a07-11eb-83a2-2a015f680623.png)

## Kullanıcı sayısı alma

![image](https://user-images.githubusercontent.com/55113204/109428321-ac5bf700-7a07-11eb-9510-641ea684f96c.png)


# GÜNCELLEME, KURMA VE KALDIRMA İŞLEMLERİ

## GÜNCELLEME

Bu komut depolarda olan yeni sürümleri günceller.

### apt-get update

yeni sürümleri kontrol edilip bildirilmiş paketlerin en son versiyonlarına günceller.

### apt-get upgrade

hem güncelleme yapar hemde sistemdeki gereksiz paketleri siler.

### apt-get dist-upgrade

depodan indirilen tüm paketlerin silinmesini sağlar sistem tertemiz olur.

### apt-get clean

eski sürüm olan artık kullanılmayan paketleri siler.

### apt-get autoclean

silinen uygulamadan geriye kalmış ve artık kullanılmayan paketleri siler.

### apt-get autoremove

-y parametresi otomatik olarak yes olarak sistemi devam ettirir bizden cevap beklemeden yes diyerek sistem kesintisiz çalışır.

## KURMA

## Depodan kurulum ile program kurmak

Sistemimiz güncel ise ve program depoda varsa apt-get install program_adı şeklinde programlarımızı kurarız. 
Programın depoda olup olmadığını kontrol etmek için apt-cache search program_adı komutu ile girer bakar kontrol ederiz. Tekrar konsola programın adını yazarak teyit edebiliriz.

## Program kaldırma

Kurulan program kaldırmak istiyorsak apt-get remove program_adı şeklinde girdiğimizde otomatik olarak kaldırırız. 
Programın yapılandırma dosyalarını sistemden kaldırmak istiyorsak apt-get - -purge remove program_adı ile kaldırabiliriz.

## Paket yönetim sistemi ile kurulum

Debian paketleme sistemine sahip olduğu için kali uzantı olarak .deb olarak kurulum gerçekleştirebiliriz.
Dpkg -i dosya_adı.deb ile program kurarız.
Dpkg -r dosya_adı ile sileriz.
/etc altındaki paketlerini de silmek istersek -p parametresi kullanırız.
Paketleri tekrar yapılandırmamız gerekirse reconfigure dosya_adı şeklinde yazarız.
-l parametresi ile tüm parametreler hakkında bilgi alırız.

Çıktıda yer alan paketlerin sol tarafındaki ifadelerin anlamı:
ii : paket normal olarak sisteme yüklendi.
rc : paket yüklendikten sonra silindi ancak konfigürasyon dosyaları halen mevcut.
pn : paket konfigürasyon dosyaları ile birlikte sistemden kaldırıldı.

Kurulu paketin durumu için dpkg -s program_adı şeklinde paketin durumunu öğrenebiliriz.

Kurulu paketin içeriğini öğrenmek istersek dpkg -L parametresini kullanırız.

Indirdiğimiz paketleri kurmadan içeriğini görmek istiyorsak dpkg -c parametresi kullanırız.

Sistemden kaldırılmış paketleri dpkg - - get – selections ile görürüz.

Bu paketi daha sonraya yedeklemek istersek dpkg - - get – selections > yedeklenecek_dosya şeklinde yazarız.

Yedeklenen dosyaları başka bir sisteme tek seferd yüklemek için;
dpkg - - set – selections > yedeklenecek_dosya

Eksik olan bişey varsa onları güncellemek için ise;
apt-get deselect-upgrade komutu ile yaparız.



# JOKER KARAKTERLERİN KULLANIMI

Tek seferde birden fazla dosyaya işlem yapan karakterlere joker karakterler denir. 
Asterix işareti : ‘*’ rm funda* yaparsak funda ile ilgili her şeyi silmiş oluruz.

![image](https://user-images.githubusercontent.com/55113204/109428425-28eed580-7a08-11eb-9a1a-b7cd9448de87.png)

? karakteri

Birbirine yakın yazılışlara yakın dosyaları görüntülememizi sağlar.

![image](https://user-images.githubusercontent.com/55113204/109428431-2e4c2000-7a08-11eb-866f-befeb41502e1.png)
 
[] karakteri

Istenilen değerler parantez içinde belirtilerek çağırılır.

![image](https://user-images.githubusercontent.com/55113204/109428443-373cf180-7a08-11eb-861f-5658ec02dbf9.png)

[!değer] burada belirtilen değerler haricindeki değerleri basar.
[değer-değer] aralıklarını basar.




# AĞ BAĞLANTI KOMUTLARI

## ifconfig Komutu

Ağ bağlantı kartlarını listelemek için kullanılır. Eth ethernet kartları hakkında bilgi vermektedir.
Lo localhost hakkında bilgi vermektedir.
Wlan0 ise kablosuz ağ hakkında bilgi vermektedir.
Ifconfig kart_adı ile tüm kartları değil istediğimiz kartı listeleyebiliriz.
Eth0 ip adresini değiştirmek istiyorsak sudo ifconfig eth0 ip_adres şeklinde yapabiliriz.
ağları kapatmak istersek ifconfig ağ_adı down yaparız. ifconfig ağ_adı up ile de geri açarız.

## Ping Komutu

Ağın ayakta olup olmadığını kontrol eden komuttur. Sınırlı sayıda pinglemek istersek -c parametresi kullanılır.
Route komutu
Sistemimizdeki ip yönlendirme tablosunun içeriğini görmemizi sağlayan komuttur.

## traceroute Komutu

Belirli bir yere gönderilen iplerin hangi hostlar üzerinden geçtiğini gösteren komuttur.

## whois Komutu

Domain hakkında bilgiler veren yani domain ne zaman kurulmuş, ne zamana kadar geçerli, kimin üzerine kayıtlı bunun gibi bilgileri verir.

## host Komutu

Host hakkında bilgi almamızı sağlar.

![image](https://user-images.githubusercontent.com/55113204/109428480-59cf0a80-7a08-11eb-818d-c460f269867c.png)

## dig Komutu

Dns kayıtlarına bakmak için kullanılan komuttur.

![image](https://user-images.githubusercontent.com/55113204/109428497-62bfdc00-7a08-11eb-9044-bd7ffffbb699.png)

## arp Komutu

Mac ve ip eşleşmesinin tablolandığı komuttur.

![image](https://user-images.githubusercontent.com/55113204/109428510-69e6ea00-7a08-11eb-9878-e11a51d8bea0.png)

## tcpdump Komutu

Sisteme yapılan ve sistemin yaptığı bağlantıları anlık olarak görüntüleyen komuttur.

![image](https://user-images.githubusercontent.com/55113204/109428526-753a1580-7a08-11eb-9712-535ba3674d5c.png)

Direk olarak bağlantıları görüntülemek istersek ise -n parametresi kullanırız.

![image](https://user-images.githubusercontent.com/55113204/109428573-a87ca480-7a08-11eb-8349-522d4c55c4d4.png)

# cron Komutu

Cron belirlenmiş zamanda belirlenmiş görevi yerine getiren komuttur.
Öncelikle cron ayakta mı değil mi ona bakıyoruz. Evet cron şu anda aktif durumda.

![image](https://user-images.githubusercontent.com/55113204/109428582-b0d4df80-7a08-11eb-9d09-df4ab41a0b02.png)

Cron dosyasının nerede olduğunu /etc dizinin içinde bulabiliriz.

![image](https://user-images.githubusercontent.com/55113204/109428590-b7fbed80-7a08-11eb-9515-e96afc3ec310.png)

Düzenleme yapmak için -e parametresini kullanırız.

![image](https://user-images.githubusercontent.com/55113204/109428594-bd593800-7a08-11eb-8aa6-5a663cc8573b.png)

Crontabları listelemek istediğimizde -l parametresini kullanırız.

![image](https://user-images.githubusercontent.com/55113204/109428599-c1855580-7a08-11eb-8374-e5e4b4d74bd9.png)

Oluşturduğumuz tüm crontabları silmek istersek -r parametresini kullanırız.



# LOG DOSYALARI

Log dosyaları kayıt dosyalarıdır. Bu dosyalarının nereden kaynaklandığını syslog konfigürasyon dosyasından bakabiliriz. 

![image](https://user-images.githubusercontent.com/55113204/109979246-bd5e7e00-7d0f-11eb-86a2-dbdd12a7bc90.png)
 
Sisteme şuanda bağlı olan kullanıcıların varlığını listeleyen log komutu /var/run ls ile bunu listelemekteyiz.

![image](https://user-images.githubusercontent.com/55113204/109979269-c3ecf580-7d0f-11eb-9b8b-259da8ceebee.png)

var/run içindeki who komutu sistemin son başlatılmasında hangi kullanıcının aktif olduğunu ve ne zaman aktif olduğunu görüntülemekteyiz. Ayrıca hangi id aldığını da görmekteyiz.

![image](https://user-images.githubusercontent.com/55113204/109979288-c8b1a980-7d0f-11eb-896a-c8e7e8363981.png)

Utmp şuandaki bağlanan kullanıcılar hakkında bilgi verirken wtmp ise daha önce bağlanmış kullanıcılar hakkında bilgi vermektedir.

![image](https://user-images.githubusercontent.com/55113204/109979308-cd765d80-7d0f-11eb-8891-face8cf14950.png)

Last hem geçmişte hemde şuanda kayıtlı ola kullanıcıları listeler.

![image](https://user-images.githubusercontent.com/55113204/109979329-d23b1180-7d0f-11eb-9fc8-c09e22224ed4.png)

Bad logların listesini lastb komutu ile bakarız.

![image](https://user-images.githubusercontent.com/55113204/109979345-d6ffc580-7d0f-11eb-84c2-a78a8323d44d.png)

Syslog ağ üzerinden gelen TCP UDP portlarını dinleyenilen bir C kütüphanesidir. 

Ryslog ise ip bazlı kısaltmalar ile herhangi bir bilgiyi log dosyasını istediğimiz bir log dosyasına yönlendirebiliriz. 


