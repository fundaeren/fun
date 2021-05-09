# Wireshark
Linux, Windows ve MacOS işletim sistemlerinde desteklenen birçok kriter çevresinde paket filtreleme sağlayan ve çeşitli formatlarda kayıt edilmesine imkan sunan,
anlık paketleri yakalayıp görünütleyebilen ve çeşitli istatistikler oluşturabilen, ağ trafiğini canlı izlenebilme ve protokol hataları, ağ içeresindeki hataları tespit edip
çözmeye yardımcı olan son olarak da tersine mühendislik çalışmaları gibi bir çok farklı konuda tercih edilen bir araçtır.

## WinPcap
Anlık olarak ağ trafiğini yakalayıp wireshark aracına gönderen kısımdır. 

Standart olarak açılan pencere terminale de yazılarak açılabilmektedir. 

İlk açılan sayfayı inceleyelim

Wireshark aracı en yetkili kişi yani root olarak çalışmaktadır. Bunun amacı wireshark aracı bizim ağ kartlarımıza erişmek istemesinden dolayıdır. 
İstenilen ağ kartlarına erişiminde kullanılan ağ kartları hakkında bilgi edinilmesini sağlayan bölüme Capture yazısına tıklayarak ulaşmaktayız.

Şimdi paket yakalamak için eth0 ağ kartını seçip firefoxa girelim ve elde edilen sonuçlarımızı bir bakalım.

Kendi filtremizi elde etmek istiyorsak eğer bunun için de wireshark bize imkan sunmaktadır.

Örnek olarak ARP paketlerini listeledik.

Kendi filtreleme butonumuzu oluşturmak için ise şu şekilde adımlar izlenmektedir.

Filtreleme butonunu silmek için ise izlenilen yol aşağıda gösterilmiştir.

Özel olarak bir kolon eklenmek istediğimiz de ise; 

MAC adresleri için aktif çözümlemesini aktifleştirmek için;

Wireshark adres çözümlemeyi kendi içerinde bulunan manuf ismindeki dosyayı sürekli güncelleyerek ve kullanarak yapmaktadır.



