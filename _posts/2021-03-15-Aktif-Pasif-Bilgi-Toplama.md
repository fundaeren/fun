




## PASİF BİLGİ TOPLAMA
Pasif bilgi toplama, bilgi topladığımız kişi veya kurumun haberi olmadan, sistemde log bırakmadan, internette açık olan bilgileri elde etmektir. Bu arama tipinde çeşitli uygulamalar ve yöntemler kullanılır. 

### theHarvester
Bu tarama aracı internet üzerindeki tüm sitelerde hedef domainde tarama işlemi yaparak önümüze listelemektedir. İstediğimiz siteleri üzerinde de yada belirlediğimiz miktarda sonuç elde edebiliriz.

![image](https://user-images.githubusercontent.com/55113204/111266760-08e02880-863c-11eb-9f76-6166a9473ffd.png)

![image](https://user-images.githubusercontent.com/55113204/111266769-0c73af80-863c-11eb-9483-af7f6025f7e6.png)

### Netcraft

Netcraf bir web sitesinin web sunucusu, ip delegasyonu, arka planda çalışan yazılımlar, işletim sistemleri gibi bilgileri vermek için kullanılır.

![image](https://user-images.githubusercontent.com/55113204/111266844-28775100-863c-11eb-9016-03e9cb158d9d.png)

### Whois 

Whois herhangi bir whois web sitesinden istediğimiz domaini girerek o domain hakkında pasif bilgiler edinmemizi sağlar.
![image](https://user-images.githubusercontent.com/55113204/111267026-74c29100-863c-11eb-87c9-3fb91636ed1e.png)

![image](https://user-images.githubusercontent.com/55113204/111266911-404ed500-863c-11eb-8448-5ebbb45d4e1f.png)

### Autowhois 

Burada da bir domain hakkındaki whois bilgilerine ulaşılmaktadır.

![image](https://user-images.githubusercontent.com/55113204/111266986-5e1c3a00-863c-11eb-9476-3ffd81140d22.png)

### Ripe 

www.ripe.com adresinde whois üzerinden elde ettiğimiz ip adresiyle arama yaptığımızda bu ip aralığına dahil olan ip bilgilerini listelemektedir.

![image](https://user-images.githubusercontent.com/55113204/111267015-6d02ec80-863c-11eb-9ec7-b4b2d39d6ace.png)

![image](https://user-images.githubusercontent.com/55113204/111267062-7d1acc00-863c-11eb-9803-cf76bd15481b.png)

### Centrol Ops 

Bu web sitesi bize girdiğimiz domain veya ip adresine göre port taraması yapmaktadır. Aynı zamanda transroute bilgilerine de ulaşılabilir.

![image](https://user-images.githubusercontent.com/55113204/111267116-93288c80-863c-11eb-9452-7e4958f35a8e.png)

![image](https://user-images.githubusercontent.com/55113204/111267142-9b80c780-863c-11eb-9f4e-d118d4529d30.png)


### SOA Kaydı

SOA kaydı bird dns serverin o bölgeden sorumlu olduğunu gösteren ilk kayıttır.yani belirli bir alandaki dns serverın parametrelerini tanımlamak için kullanılır. O bölgedeki zone server ismi, seri numarası olan serial değeri bu değer yapılan her değişiklikte kendini bir arttırması gerekir, refresh ayarlama yapılan dosyaların kendini ne kadar sürede bir yenileyeceğini, retry bu alanda ne kadar sürede bir aramının kendini tekrarlayacağı, ttl değeri  belirlenen süre kadar cache tutabileceği, expire değeri ise ne kadar süre sonra aramının durduracağını belirtir.

### MX Kaydı

MX kaydı alan adına gelen e-postaları hangi servera iletebileceğinizi gösteren kayıttır. Burada exchange alanında alt1.aspmx.L.google.com e-posta sunucusunun adresidir. Preference yada prority değeri ise hangi öncelik sırasında sunuculara yönlendireceğini belirten değerdir. Birden fazla mx kaydı olabilir böyle bir durumda öncelikle preference değeri en düşük olan sunucuya ondan cevap alınmaz ise sıralamadaki diğer sunucuya iletilir.

### A Kaydı

A kaydı host adını bir addresse yönlendirir. Yani A address kaydıdır. Burada 192.124.249.10 ipsini alan adına bağlı bir alt alan adının bu ip adresine yönlendirebileceği bilgisini içerir. En çok kullanılan kayıt türüdür. Yani www olarak girdiğimiz bir web sayfasında biz www.kali.org olarak giriyorsak aslında bu ip adresi üzerinden gidiyoruz. Biz ip lerini ezberlemek yerine isimler üzerinden istediğimiz adrese giriş yapmaktayız.

### CNAME Kaydı

Cname kaydı bu kayıt A kaydının kapsadığı özelleşmiş kayıtlar diyebiliriz. Bir A kaydı olmadan Cname kayıtları olamaz missal verecek olursak;
Domain.com A 192.124.249.10
1. Mail.domain.com Cname domain.com
2. ftp.domain.com Cname domain.com
3. ssh.domain.com Cname domain.com 

Gibi Cname kayıtları vasıtasıyla bu domaindeki özelleşmiş alt domainlerdir. A kaydı olmadan Cname kayıtları da olmaz. Cname kayıtlarınız yoksa bu tip adresleri kullarakta dns serverınıza bağlanamazsınız.

### TXT Kaydı

Txt kayıtları e-postalar üzerinde spamlı e-postaların kayıtlarını tutan SPF kayıtlarını tanımlamak için kullanılmıştır.

### PTR Kaydı

Ptr kayıtları bir ip ile domain isimlerini eşleştiren kayıtlardır. Yani şu ip adresindeki dns serverın ismi nedir diye sorduğumuzda ptr kayıtlarından bakabiliriz. A kaydının tersidir. A kaydında domain ismine ip adresi bulunuyordu. Burada ip adresine domain ismi bulunuyor.

### NS Kaydı

Ns kayıtları ağ üzerinde olan ve kullanım halinde olan dns serverları tanımlamaktadır. Ip adreslerine göre sorgulama yapar ve o ip adreslerinin karşılığındaki server hangi server ise onu bulur. Ns kayıtlarının değiştirilmesine gerek yoktur çünkü sitenin durmasına sebep olabilmektedir.

### AAA Kaydı

AAA kayıdı ise ipv6 kullanılmak üzere tanımlanmış A kaydı ile aynı görevi yapan address kayıtlarıdır.

![image](https://user-images.githubusercontent.com/55113204/111267925-b0aa2600-863d-11eb-9dda-7a9a87aecafa.png)

Traceroute bilgilerini de alabiliyoruz.

![image](https://user-images.githubusercontent.com/55113204/111268023-ccadc780-863d-11eb-95ec-6b3c3dbfd360.png)

### OTR

Otr mesajları şifreleme protokolüdür. 

### SSL Shopper

Bir domain ssl sertifakasını kontrol etmek için kullanılan web sitelerinden bir tanesidir.

![image](https://user-images.githubusercontent.com/55113204/111268107-e949ff80-863d-11eb-8da7-a2cc60f388e8.png)

### Robtex 

Robtex sitesi bu site dns bilgilerini grafiksel olarak gösteren sitedir.

![image](https://user-images.githubusercontent.com/55113204/111268162-fd8dfc80-863d-11eb-86cd-577ded6a8da4.png)

### Wayback Machine 


Wayback machine sitesi araştırılan bir web sitesi hakkında eskiden web sayfasının yada paylaşılan bilgilerinin ne olduğu hakkında geçmiş bilgilerine ulaşmamızı sağlayan web sitesidir. Burada istediğimiz tarihe girip daha önce sayfa nasılmış neler yayınlanmış bunlar hakkında geçmişe dönük bilgi edinebiliriz. 

![image](https://user-images.githubusercontent.com/55113204/111268228-10a0cc80-863e-11eb-99fd-32ec62c0a6d4.png)

### Dnsdumpster

Dnsdumpster sitesi domain bilgilerini ve bu domane bağlantılı serverların listesini ve bilgilerini göstermektedir.

![image](https://user-images.githubusercontent.com/55113204/111268364-3d54e400-863e-11eb-96a7-4f4f8d61f5b7.png)

Alt tarafa inildiğinde girdiğimiz domain hakkında şematize edilmiş görsel bulunmaktadır.

![image](https://user-images.githubusercontent.com/55113204/111268400-4a71d300-863e-11eb-9701-9a29e9025a20.png)

### Google Dorks

Arama motorlarından bilgi toplama pasif bilgi toplamada en kritik bilgi toplama tekniğidir. İstediğimiz bilgi hakkında belirli kriterler girerek istediğimiz sonuçlara ulaşmada etkin bir rol oynanır.

### site

Belirli bir web sitesi hakkında bilgi toplamak istiyorsak site:domain olarak google tarayıcısında arama yaptığımızda sadece o site hakkında bilgiler elde etmekteyiz.

![image](https://user-images.githubusercontent.com/55113204/111268564-7db46200-863e-11eb-9db2-d2d95a4b594f.png)

### inurl

Url sinde olan değeri listelemek için inurl:aramak_istediğimiz_değer şeklinde yazarsak url sinde o kelime olan bilgiler listelenir.

![image](https://user-images.githubusercontent.com/55113204/111268628-8f960500-863e-11eb-8436-20f025eec8b2.png)

### intitle

Bir klasör şeklinde yani içinde bilgiler bulunduran bir başlık araması yapmak istiyorsak intitle:kelime şeklinde arama yapabiliriz.

![image](https://user-images.githubusercontent.com/55113204/111268660-9b81c700-863e-11eb-9891-406599449547.png)

### intext

Aradığımız kelime herhangi bir web sitesinin herhangi bir yerinde geçiyorsa bile onunla ilgili bilgileri bize vermektedir.

![image](https://user-images.githubusercontent.com/55113204/111268703-ac323d00-863e-11eb-9a6e-1586b9187982.png)

### filetype

Dosya tipine göre belirli bir hedef domainde arama yapabiliriz. Bunun için filetype:dosya_tipi site:hedef_domain şeklinde arama yapabiliriz.

![image](https://user-images.githubusercontent.com/55113204/111268749-beac7680-863e-11eb-8b4c-7bfde72c4c16.png)

### info

Domain hakkında özet bilgiler elde etmek istiyorsak info:domain_name şeklinde arama yapabiliriz.

![image](https://user-images.githubusercontent.com/55113204/111268786-ccfa9280-863e-11eb-966a-4f62a130122a.png)

### link

Farklı sitelerdeki aradığımız domaini kullanmış siteleri göstermek için link:domain_name şeklinde arama yapabiliriz.

![image](https://user-images.githubusercontent.com/55113204/111268838-de439f00-863e-11eb-82b9-76fb30342ce8.png)

### related

Aradığımız siteye içerik yönünden benzeyen sitelerin listesini görmek istiyorsak related:site_ismi şeklinde arama yapabiliriz.

![image](https://user-images.githubusercontent.com/55113204/111268868-eac7f780-863e-11eb-8a29-776e9b455df1.png)

### or

Kelime1 or kelime2 şeklinde arama yaptığımızda bu iki kelimenin de içinde geçtiği sonuçları elde ederiz.

![image](https://user-images.githubusercontent.com/55113204/111268932-ff0bf480-863e-11eb-803c-2cfa3cd8aa58.png)

### xls araması 

Bir site üzerinde filetype xls olan arama yapabiliriz.

![image](https://user-images.githubusercontent.com/55113204/111269017-1945d280-863f-11eb-8586-d4b25e539f94.png)

### AND

Ortak bir çıktı elde edinmek için and operatörü kullanılabilir.

![image](https://user-images.githubusercontent.com/55113204/111269163-4a260780-863f-11eb-9f58-d07e9df82bb9.png)

### admin paneli

Admin panelini açmak için google dork kullanılabilir.

![image](https://user-images.githubusercontent.com/55113204/111269244-675ad600-863f-11eb-8095-5a588916c2c4.png)

![image](https://user-images.githubusercontent.com/55113204/111269517-cddff400-863f-11eb-90b4-4c8a8c12f542.png)

![image](https://user-images.githubusercontent.com/55113204/111269531-d20c1180-863f-11eb-9c51-3c3c906dab60.png)

![image](https://user-images.githubusercontent.com/55113204/111269552-d6d0c580-863f-11eb-8580-7403f3dbc87c.png)

![image](https://user-images.githubusercontent.com/55113204/111269562-da644c80-863f-11eb-88ce-3f455bf19732.png)

![image](https://user-images.githubusercontent.com/55113204/111269573-df290080-863f-11eb-86f5-426fe7a7e4b3.png)



### loc
Loc parametresi belirli bir alan üzerinde arama yapan parametredir.

### daterange

Daterange:belirli bir zaman aralığını veren tarama parametresidir.

### phonebook

Phonebook ile telefon numaralarına ulaşılabilir.


Arama sonuçlarında çok fazla sonuç elde ettiğimizde bunu istediğimiz şekilde filtreleyebiliriz. Örneğin blog olanları göstermek istediğimizde şu şekilde bir script yazarız.

![image](https://user-images.githubusercontent.com/55113204/111269477-bc96e780-863f-11eb-95c0-2502d553ee4b.png)

![image](https://user-images.githubusercontent.com/55113204/111269487-c02a6e80-863f-11eb-8a03-5fa0455302ad.png)


İstenilen bir kurumdan istenirse tc kimlik numaraları public olarak yayınlanmışsa elde edilebilir.

![image](https://user-images.githubusercontent.com/55113204/111269671-f7008480-863f-11eb-87c1-e50d507297ba.png)

Önbelliğine bakmak istersek cache:hedef_site olarak girilir.

![image](https://user-images.githubusercontent.com/55113204/111269734-0384dd00-8640-11eb-8a68-192e64d68f7a.png)

![image](https://user-images.githubusercontent.com/55113204/111269774-113a6280-8640-11eb-8e44-8a9c9a7c3fe5.png)

### allinurl

allinurl parametresinde urlsinde belirttiğimiz tüm karakterleri içeren sonuçları verir.

![image](https://user-images.githubusercontent.com/55113204/111269856-2a431380-8640-11eb-89e7-28053adefa3d.png)

### inanchor

inanchor bu bir bağlantıda tam bir bağlantı metnini aradığımızda kullanılır.

![image](https://user-images.githubusercontent.com/55113204/111269927-434bc480-8640-11eb-90c3-6604267b9606.png)

### *

“*” ifadesi belirtilen kelime ile alakalı herhangibir şeyi bul bana göster demektir.

![image](https://user-images.githubusercontent.com/55113204/111269972-53fc3a80-8640-11eb-9f9f-b65db12734d6.png)

### Shodan

Shodan internete açık olan bilgileri tarayan ve nmap taramalarını görselleştiren bir arama motorudur.

![image](https://user-images.githubusercontent.com/55113204/111270046-6bd3be80-8640-11eb-95ba-93b34ca50999.png)

![image](https://user-images.githubusercontent.com/55113204/111270060-71310900-8640-11eb-8eea-a92da6db3ba6.png)

![image](https://user-images.githubusercontent.com/55113204/111270079-755d2680-8640-11eb-99ce-cc9c0cfedd67.png)

### Maltego

Maltego hem aktif hem pasif aramada aktif rol oynayan bir tarama aracıdır. Maltego ile ip bilgilerini, whois bilgilerini, alan adlarını, ağın tespitini tespit edilmesi, e-posta, telefon, fax numaraların,sosyal paylaşım alanlarında paylaşımlarını,internet alt yapısını kullanarak domainlerini öğrenebiliriz. 
Burada olduğu  gibi ip aralıklarında bulunan tüm domain adreslerini görmekteyiz.

![image](https://user-images.githubusercontent.com/55113204/111270369-d38a0980-8640-11eb-96f2-8598931a7884.png)

![image](https://user-images.githubusercontent.com/55113204/111270384-d684fa00-8640-11eb-8e6e-95f7922ae2e7.png)

Yukarıda gazi üniversitesinde bulunan e-mail,domain,location, ip adresleri gibi bilgileri listelemek istediğimiz bilgilere göre kullanabiliriz. Misal burada bir mailden onun kullanıcısına oradan o mailin nereye ait olduğuna ve locationa gittik.

![image](https://user-images.githubusercontent.com/55113204/111270480-f6b4b900-8640-11eb-9fb8-59387b012b1e.png)

## AKTİF BİLGİ TOPLAMA

### Netdiscover

Netdiscover yerel ağdan veya yerel ağ dışından erişerek bir ağdaki aktif makineleri listelemek için kullanırız. Hem aktif hem pasif arama aracıdır. Burada kalide kurulu olarak gelen araçtır. Bir parametreyle yada parametresiz de yazılabilir. 

![image](https://user-images.githubusercontent.com/55113204/111270530-08965c00-8641-11eb-9940-c3418f2ea78f.png)

![image](https://user-images.githubusercontent.com/55113204/111270541-0b914c80-8641-11eb-9e67-52e498c0d18b.png)

### Dimitry

Dimitry aracı port taraması yapar. Dimitry domain şeklinde arama yapılabilir. Aynı zamanda domain ve ip bilgileri gibi önemli bilgilere de ulaşılabilir.

![image](https://user-images.githubusercontent.com/55113204/111270900-7fcbf000-8641-11eb-81ef-d19558a0d3ac.png)

### Fierce
Fierce hedef web sitesindeki dns suncularının bulunmasını ve zone transfer yapılmasını sağlamaktadır. Belirtilen aralık içinde geriye doğru arama yapmaktadır. Dahili ve harici olan ip aralıklarını da taramaktadır.
Burada hedefin subdomainlerinin maillerini arattık.

![image](https://user-images.githubusercontent.com/55113204/111271079-c28dc800-8641-11eb-903c-cfd7715490f6.png)

Aşağıda daha geniş bir alan üzerinde arama yaparak hedef domain hakkında bilgi edindik.

![image](https://user-images.githubusercontent.com/55113204/111271178-e5b87780-8641-11eb-9937-f577f7624aad.png)

Burada ise hedef domain hakkında genel bilgiler edindik.

![image](https://user-images.githubusercontent.com/55113204/111271235-f5d05700-8641-11eb-86e4-ecf704dae06f.png)

### Nmap
Nmap ağ keşfini sağlayan açık kaynaklı bir yazılımdır. Uzun yıllardır kullanılan en önemli araçlardandır. Ağdaki cihazların, onların açık kapalı olarak port durumlarını, portlardan çalışan uygulamalarını, versiyon numarını, işletim sisteminin tespiti ve hangi version kullanıldığını bu versiyonların zaafiyetini öğrenmek için kullanılan önemli bir ağ tarama aracıdır. Nmap görselleşmiş  halinde grafik arayüzlü programına da zenmap denmektedir.

Bazı en çok kullanılan portların numaraları verecek olursak; ftp21, ssh 22, telnet 23, smtp 25, dns 53, http 80, pop3 110, sftp 115, rpc 135, ımap 143, ırc 194, ssl 443, smb 445, mssql 1443, mysql 3306, remote desktop 3389.

Tcp syn scan da port açıksa syn paketi gönderilir karşı tarafta bağlantı kurabilmek için syn/ack döndürür. Burada üç yollu el sıkışma yoktur çünkü portun açık olduğu bilgisini almıştır bundan dolayı sürekli karşı taraf syn/ack yollamasın diye bağlantıyı koparmak için rst paketi gönderir. Üç yollu el sıkışma tamamlanmadığından dolayı yarı açık tarama da denir.

Eğer port kapalı ise syn paketi gönderildiğinde karşı makine rst paketi göndererek bu port kapalı demektedir. Ve iletişim bitmektedir.

Port filtreli ise saldırgan porta syn paketi gönderir hedeften dönüş olmadığında, trafikten koptuğu düşünüldüğünden bi süre bekler ve tekrar syn paketi yollar yine cevap gelmezse filtreli diye düşünür ve devam eder. Port filtreli ise portun önünde güvenlik cihazı olan firewall, ips, ids gibi cihazlar girer ve nmap hedef sistemin portu ile iletişime geçemez.

-sS taramasında root yada admin olarak giriş yapıldığında default olarak yapılan taramadır. s harfi scan yapmamızı S harfi ise syn taraması yapmamızı sağlamaktadır. Biz burada açık olan portlar nelermiş onları öğrenmek için -sS parametresi ile tarama, hedef domaine port taraması yapmaktayız. Burada syn, syn-ack,rst bayrakları gönderildiğinden dolayı tam bağlantı kurulamamıştır bundan dolayı yarı üçlü el sıkışma denmektedir.

![image](https://user-images.githubusercontent.com/55113204/111271641-89098c80-8642-11eb-9aca-bdb420cc9777.png)

-sT taraması yani TCP connect taraması, root yada admin olarak giriş yapılmadığı zaman default olarak yapılan taramadır. Bu taramada nmap paketler üzerinde kontrole daha az sahip olduğundan dolayı syn taraması daha çok tercih edilmektedir. Daha uzun süreli ve daha fazla paket gerektirmesinin sebebi tam bağlantı kurmasından dolayıdır. -sT taraması hedef domainde bağlandıktan sonra hiçbir veri göndermeden bağlantıyı koparır bu da log kaydının tutulmasını sağlamaktadır. Burada syn, syn-ack, ack, data şeklinde bir bağlantı kurulup hemen rst bayrağı gönderildiğinden dolayı tam bir bağlantı kuruluyor normalde finish bayrağı bağlantı kurduğunu söyler fakar burada rst bayrak ile bağlantı hemen kopar bu tarama syn taramasının iki katı tarama yapmaktadır. Syn taramasından tek fark tam bağlantı kurulmasıdır.

![image](https://user-images.githubusercontent.com/55113204/111271860-d84fbd00-8642-11eb-90b4-1b3fe520f48a.png)

Udp de tcp de olduğu gibi bayraklar yoktur burada hedef portlara UDP paketleri göndererek port taraması yapılır. Genelde boş paketler gönderir ama daha yaygın portlar için protokole özgü paketler göndermektedir. Port açıksa UDP paketine UDP cevabı döner. Portun kapalı olması ise UDP paketine karşılık ICPM Destination Unreachable yada Port Uncreachable cevabı dönmesidir. UDP paketine herhangi cevap dönmezse tekrar UDP paketi gönderir yine buna cevap gelmezse portun durumunun open filtered olduğu belirlenir. Eğer portlardan ICMP unreachable errors gelirse filtreli olduğunu anlıyoruz ki bunların tipleri de type 3, code 1, 2, 9, 10, veya 13’tür. 

Nmapte -sU taraması UDP protokolü üzerinden tarama yapmaktadır. UDP taraması TCP den daha yavaştır. UDP te bağlantı kurulmadan önce kurulan anlaşma bayrakları yoktur burada sadece paketler vardır. Eğer port açıksa bağlantı kuruluyor kapalıysa paketi kabul etmediğinden bağlantı kurulamıyor.

![image](https://user-images.githubusercontent.com/55113204/111272202-51e7ab00-8643-11eb-9abf-d9a4fb4053f4.png)

Portun açık yada kapalı olduğunu anlamak için fin taraması yapılır. Hedef porta bir finsh bayrağı yollar hedeften gelen yanıta göre portun açık yada kapalı olduğunu belirler. Rst,ack bayrağı dönerse port kapalı olduğunu cevap dönmezse açık olduğunu anlıyoruz. -sF tarama parametresi kullanılır.

![image](https://user-images.githubusercontent.com/55113204/111272286-7479c400-8643-11eb-8917-3bac76742d60.png)

Null taramasında hedef porta sıfır değerindeki null bayrağı gönderir. Hedef port nasıl cevap vereceğini bilmediğinden hedefin açık olduğuna dair herhangi bir cevap göndermeyecektir. -sN şeklinde tarama parametresi kullanılır.

![image](https://user-images.githubusercontent.com/55113204/111272316-822f4980-8643-11eb-821f-20a8a222e23e.png)

XMAS taramasında ise nmap hedef porta PSH, URG ve FIN bayraklarını toplu olarak göndermektedir. Bunun parametresi -sX kullanılır. Bu tarama noel ağacı olarakta nitelendirilmektedir. Toplu olarak gönderilen bu bayrakların sonucunda eğer ki port açıksa hedeften herhangi bir dönüş olmayacaktır. Port kapalı ise rst,ack geri dönütü olacaktır.

![image](https://user-images.githubusercontent.com/55113204/111272395-a3903580-8643-11eb-808d-b10293edadd5.png)

Nmap ile ip adresine göre tarama yapılırken o ip adresinin çalışır durumda olup olmadığı ve çalışan servislerin bilgilerini getirmektedir.  Burada 1000 tane port taradı ve bundan 4 tanesinin açık olduğunu geriye kalan 996 tanesinin filtreli olduğunu bize gösterdi.

![image](https://user-images.githubusercontent.com/55113204/111272470-ba368c80-8643-11eb-826c-2c4584044296.png)

### Mascan

Mascan nmap gibi ama nmap kadar gelişmemiş olmakla hedefin port durumunu ve tarama hızlarının ayarlanabileceği bir araçtır. Burada 194.27.18.16 ip adresinin 53. Portunun taramasını yapmaktayız.

![image](https://user-images.githubusercontent.com/55113204/111272574-df2aff80-8643-11eb-9e12-39b7b6201d2e.png)

Burada 194.27.18.16 ip adresli gazi üniversitesinin 1000 portunu 500paket/saniye süresinde taramış bulunmaktayız. 

![image](https://user-images.githubusercontent.com/55113204/111272639-f0740c00-8643-11eb-9f40-34442f62b0f5.png)

Birden fazla port taraması da yapabiliriz.

![image](https://user-images.githubusercontent.com/55113204/111272719-097cbd00-8644-11eb-9751-8bf82ae5b606.png)

### DNS sunucuları hakkında bilgi toplama

Dns kayıtlarına bakmak için dig komutu kullanılabilir.  Burada dig komutu ve domain adını kullanarak A kaydına ulaşabiliriz.

![image](https://user-images.githubusercontent.com/55113204/111272782-1a2d3300-8644-11eb-9f08-e582276abd9f.png)

Dig komutu ile name serverlar hakkında bilgi edinmek istiyorsak -t NS parametresini kullanırız.

![image](https://user-images.githubusercontent.com/55113204/111272820-25805e80-8644-11eb-9634-300b4909ce45.png)

Dig komutu ile MX kayıtlarına ulaşabiliriz.

![image](https://user-images.githubusercontent.com/55113204/111272874-34671100-8644-11eb-9da0-4c4737a27438.png)

Dns zone dns veritabanındaki kayıtların bir serverdan başka servera aktarılmasıdır. 

![image](https://user-images.githubusercontent.com/55113204/111272931-434dc380-8644-11eb-8c0b-59fdc6f26994.png)

### Nslookup

Bağlantı sorunu yaşayan domainlerde inceleme yapmak için nslookup aracı kullanılabilir. Domain adı ve ip adresleri ile eşleşme yapmak için de kullanılır.

![image](https://user-images.githubusercontent.com/55113204/111273075-6d06ea80-8644-11eb-886d-37715505ed3f.png)

Nslookup ile istediğimiz domain ile domain hakkında ne tür bilgi istiyorsak ona erişebiliriz. Ben burada ns bilgilerine ulaşmak istedim. Bana hem name serverların domainlerine hemde ip adreslerine ulaştım. Bu şekilde nslookup kullanımına etkişimli mod denmektedir.

![image](https://user-images.githubusercontent.com/55113204/111273452-e6064200-8644-11eb-96a2-27258d23d58e.png)

Nslookup etkileşimsiz mod olarak ise domain adından önce kullanmamız gereken parametre -query=? şeklindedir. Burada ? ile belirtilen alana ne tür bir bilgi almak istiyorsak örneğin mx kayıtlarına ulaşmak istiyorsak onun hakkında bilgi edinmiş oluruz.

![image](https://user-images.githubusercontent.com/55113204/111273730-37aecc80-8645-11eb-8994-1a87f7880df6.png)

Tüm dns kayıtları hakkında bilgi edinmek istiyorsak şu şekilde bir arama yapmaktayız.

![image](https://user-images.githubusercontent.com/55113204/111273768-45645200-8645-11eb-832d-6ae9f9fb6c67.png)
