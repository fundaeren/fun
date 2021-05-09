# Wireshark
Linux, Windows ve MacOS işletim sistemlerinde desteklenen birçok kriter çevresinde paket filtreleme sağlayan ve çeşitli formatlarda kayıt edilmesine imkan sunan,
anlık paketleri yakalayıp görünütleyebilen ve çeşitli istatistikler oluşturabilen, ağ trafiğini canlı izlenebilme ve protokol hataları, ağ içeresindeki hataları tespit edip
çözmeye yardımcı olan son olarak da tersine mühendislik çalışmaları gibi bir çok farklı konuda tercih edilen bir araçtır.

## WinPcap
 Anlık olarak ağ trafiğini yakalayıp wireshark aracına gönderen kısımdır. 
 
## Wireshark Ayrıntılı İnceleme

 Standart olarak açılan pencere terminale de yazılarak açılabilmektedir. 

![wire1](https://user-images.githubusercontent.com/55113204/117575551-07d2f100-b0eb-11eb-8ddc-566e2ac5f692.PNG)


İlk açılan sayfayı inceleyelim.

![wire2](https://user-images.githubusercontent.com/55113204/117575563-128d8600-b0eb-11eb-8c78-b8f3ef9c2596.PNG)


Wireshark aracı en yetkili kişi yani root olarak çalışmaktadır. Bunun amacı wireshark aracı bizim ağ kartlarımıza erişmek istemesinden dolayıdır. 
İstenilen ağ kartlarına erişiminde kullanılan ağ kartları hakkında bilgi edinilmesini sağlayan bölüme Capture yazısına tıklayarak ulaşmaktayız.

![wire3](https://user-images.githubusercontent.com/55113204/117575584-2638ec80-b0eb-11eb-98f4-9cb0df3b5e20.PNG)


Şimdi paket yakalamak için eth0 ağ kartını seçip firefoxa girelim ve elde edilen sonuçlarımızı bir bakalım.

![wire4](https://user-images.githubusercontent.com/55113204/117575608-423c8e00-b0eb-11eb-97dc-f1e5fc03544f.PNG)

![wire5](https://user-images.githubusercontent.com/55113204/117575624-4ec0e680-b0eb-11eb-8801-ec7e103769de.PNG)


Kendi filtremizi elde etmek istiyorsak eğer bunun için de wireshark bize imkan sunmaktadır.

![wire6](https://user-images.githubusercontent.com/55113204/117575644-6009f300-b0eb-11eb-9914-f950e4fd78ec.PNG)


Örnek olarak ARP paketlerini listeledik.

![wire7](https://user-images.githubusercontent.com/55113204/117575650-69935b00-b0eb-11eb-98e4-a11240ed71e5.PNG)


Kendi filtreleme butonumuzu oluşturmak için ise şu şekilde adımlar izlenmektedir.

![wire8](https://user-images.githubusercontent.com/55113204/117575663-7617b380-b0eb-11eb-8a5c-44a28fc1c896.PNG)

![wire9](https://user-images.githubusercontent.com/55113204/117575673-816adf00-b0eb-11eb-83de-ad4e65ab674f.PNG)


Filtreleme butonunu silmek için ise izlenilen yol aşağıda gösterilmiştir.

![wire10](https://user-images.githubusercontent.com/55113204/117575679-8d56a100-b0eb-11eb-9dff-80bf3b5c3035.PNG)


Özel olarak bir kolon eklenmek istediğimiz de ise;

![wire11](https://user-images.githubusercontent.com/55113204/117575684-9b0c2680-b0eb-11eb-822e-cc73a676e469.PNG)


MAC adresleri için aktif çözümlemesini aktifleştirmek için;

![wire12](https://user-images.githubusercontent.com/55113204/117575691-a3646180-b0eb-11eb-9b8c-7d6686895a77.PNG)


Wireshark adres çözümlemeyi kendi içerinde bulunan manuf ismindeki dosyayı sürekli güncelleyerek ve kullanarak yapmaktadır.

![wire13](https://user-images.githubusercontent.com/55113204/117575696-acedc980-b0eb-11eb-9768-58b0820b6d59.PNG)


HTTP isteklerini analiz etmek istiyorsak eğer şu şekilde bir yol izlenebilir.

![wire14](https://user-images.githubusercontent.com/55113204/117575704-b7a85e80-b0eb-11eb-826d-c0b9277a0a03.PNG)

![wire15](https://user-images.githubusercontent.com/55113204/117575713-c0009980-b0eb-11eb-8dbe-2ee7bc017992.PNG)


Diğer bir analizleme yöntemi ise Packet Counter seçeneğidir.

![wire16](https://user-images.githubusercontent.com/55113204/117575723-ca229800-b0eb-11eb-94ca-b1ae61525717.PNG)

![wire17](https://user-images.githubusercontent.com/55113204/117575737-d0187900-b0eb-11eb-9185-20cbf9d8a1b7.PNG)


IP adreslerini analiz etmek istersek eğer aşağıdaki şekildeki gibi IPv4 yolunu takip ederek ALL Addresses seçeneğinden istediğimiz sonuçları elde edebiliriz.

![wire18](https://user-images.githubusercontent.com/55113204/117575743-da3a7780-b0eb-11eb-9111-4c515ea0d58e.PNG)

![wire19](https://user-images.githubusercontent.com/55113204/117575750-e0c8ef00-b0eb-11eb-813d-9aa4d64628c8.PNG)


Wiresharkta e hangi protokolden kaç tane paket olduğunu görmek istiyorsak Protocol Hierarchy seçeneği bize yardımcı olmaktadır.

![wire20](https://user-images.githubusercontent.com/55113204/117575759-e9b9c080-b0eb-11eb-99ed-4637cbe7dbf4.PNG)

![wire21](https://user-images.githubusercontent.com/55113204/117575769-f1796500-b0eb-11eb-8094-f4100349e6f6.PNG)


Yakalanan paketlerin özet bilgilerine ulaşmak istiyorsak Capture File Properties alanı seçilmelidir.

![wire22](https://user-images.githubusercontent.com/55113204/117575789-0229db00-b0ec-11eb-8db3-abe331843777.PNG)

![wire23](https://user-images.githubusercontent.com/55113204/117575794-08b85280-b0ec-11eb-9d44-c31c7f07e91e.PNG)


Tüm paketlerin adres çözümlemesini yapmak istiyorsak elde aşağıdaki yolu izlemeliyiz.

![wire24](https://user-images.githubusercontent.com/55113204/117575803-1077f700-b0ec-11eb-92be-878476ab4998.PNG)

![wire25](https://user-images.githubusercontent.com/55113204/117575814-18379b80-b0ec-11eb-9cf6-17c5eecb489d.PNG)


Ağınıza ait ARP saldırılarını gözlemlemek için şu filtreler kullanılabilmektedir.

![wire27](https://user-images.githubusercontent.com/55113204/117575831-2980a800-b0ec-11eb-97e7-51d4fcfd508a.PNG)

![wire26](https://user-images.githubusercontent.com/55113204/117575832-2a193e80-b0ec-11eb-8d55-6416c31bd6fd.PNG)


Wireshark ile ağın trafiği içindeki bazı paketleri export etmek istersek eğer aşağıdaki yolu kullanabiliriz. 

![wire28](https://user-images.githubusercontent.com/55113204/117575847-356c6a00-b0ec-11eb-94f3-6910a633bf2c.PNG)

![wire29](https://user-images.githubusercontent.com/55113204/117575862-3ef5d200-b0ec-11eb-84c6-72d84df22935.PNG)

Bir diğer export etme yöntemi ise sadece seçilen paketin export edilmesidir.

![wire30](https://user-images.githubusercontent.com/55113204/117575889-53d26580-b0ec-11eb-9320-3dc7e1f482c8.PNG)

![wire31](https://user-images.githubusercontent.com/55113204/117575898-5c2aa080-b0ec-11eb-831f-74774ce8cdcd.PNG)

Başka bir export etme yöntemi ise belirli bir aralıktaki paketlerin export edilmesidir.

![wire32](https://user-images.githubusercontent.com/55113204/117575920-7e242300-b0ec-11eb-842c-1e010982d55a.PNG)

Yada belirli bir paketlerin export edilmesi de yapılabilir.

![wire33](https://user-images.githubusercontent.com/55113204/117575962-9eec7880-b0ec-11eb-810c-9cb0bea358b5.PNG)

Sadece paketin üstüne tıklayarakta export edilip paket seçilme işlemi yapılabilir.

![wire34](https://user-images.githubusercontent.com/55113204/117575994-c8a59f80-b0ec-11eb-91b8-7969a1da48c0.PNG)

Burada da sadece benim işaretlediklerim seçilmektedir.

![wire35](https://user-images.githubusercontent.com/55113204/117576000-ce02ea00-b0ec-11eb-8af0-d6d2ff94f60a.PNG)


İki .pcap paketi birleştirmek için mergecap isimli araç kullanılarak farklı bir dosyaya atılabilir.

![wire36](https://user-images.githubusercontent.com/55113204/117576073-191cfd00-b0ed-11eb-9e3a-24fc47092519.PNG)


.pcap paketlerini okumak için ise capinfos aracı kullanılır.

![wire37](https://user-images.githubusercontent.com/55113204/117576083-20dca180-b0ed-11eb-80f4-a749594e210b.PNG)

## DHCP İçin Kullanılabilecek Filtreler
![wire40](https://user-images.githubusercontent.com/55113204/117576273-fe975380-b0ed-11eb-9424-d8d1f0f11b2b.PNG)

![wire41](https://user-images.githubusercontent.com/55113204/117576275-fe975380-b0ed-11eb-9f5c-07adb3ed1ca5.PNG)

![wire42](https://user-images.githubusercontent.com/55113204/117576276-ff2fea00-b0ed-11eb-83f5-7b2b7d6872f3.PNG)

![wire43](https://user-images.githubusercontent.com/55113204/117576278-ff2fea00-b0ed-11eb-8f45-b23f750bfbcb.PNG)

![wire44](https://user-images.githubusercontent.com/55113204/117576279-ffc88080-b0ed-11eb-8511-f7b23c76d147.PNG)

![wire38](https://user-images.githubusercontent.com/55113204/117576280-ffc88080-b0ed-11eb-8b0a-5a66cc6d1a84.PNG)

![wire39](https://user-images.githubusercontent.com/55113204/117576281-ffc88080-b0ed-11eb-99f7-894f049808ca.PNG)

## HTTP İçin Kullanılabilecek Filtreler
![wire48](https://user-images.githubusercontent.com/55113204/117576404-8aa97b00-b0ee-11eb-9700-161acadc849f.PNG)

![wire49](https://user-images.githubusercontent.com/55113204/117576406-8aa97b00-b0ee-11eb-9fc4-8c13b700fc71.PNG)

![wire50](https://user-images.githubusercontent.com/55113204/117576407-8b421180-b0ee-11eb-8add-ae0ad0b0c14e.PNG)

![wire45](https://user-images.githubusercontent.com/55113204/117576408-8b421180-b0ee-11eb-8d6c-a8db4abe9440.PNG)

![wire46](https://user-images.githubusercontent.com/55113204/117576409-8bdaa800-b0ee-11eb-9517-205aeb2e2d29.PNG)

![wire47](https://user-images.githubusercontent.com/55113204/117576410-8bdaa800-b0ee-11eb-8e8f-1a5e375a0ebc.PNG)

## ARP İçin Kullanılabilecek Filtreler
![wire55](https://user-images.githubusercontent.com/55113204/117576580-2c30cc80-b0ef-11eb-9233-6435b1db9a1e.PNG)

![wire56](https://user-images.githubusercontent.com/55113204/117576581-2cc96300-b0ef-11eb-94b0-c7a91ba55ef6.PNG)

![wire51](https://user-images.githubusercontent.com/55113204/117576583-2d61f980-b0ef-11eb-8ed5-aa571d036445.PNG)

![wire52](https://user-images.githubusercontent.com/55113204/117576585-2d61f980-b0ef-11eb-883e-21f7ce6bcce0.PNG)

![wire53](https://user-images.githubusercontent.com/55113204/117576586-2d61f980-b0ef-11eb-9339-a696d0760850.PNG)

![wire54](https://user-images.githubusercontent.com/55113204/117576587-2dfa9000-b0ef-11eb-87c5-fb24b7720c0d.PNG)

## DNS İçin Kullanılabilecek Filtreler
![wire58](https://user-images.githubusercontent.com/55113204/117576742-ba0cb780-b0ef-11eb-9614-c5f701153221.PNG)

![wire59](https://user-images.githubusercontent.com/55113204/117576745-baa54e00-b0ef-11eb-954a-08889dd81b64.PNG)

![wire60](https://user-images.githubusercontent.com/55113204/117576746-baa54e00-b0ef-11eb-89b0-3ce2265a6f72.PNG)

![wire57](https://user-images.githubusercontent.com/55113204/117576747-baa54e00-b0ef-11eb-828b-17ea7cb7095f.PNG)

## İnternet Protokol İçin Kullanılabilecek Filtreler
![wire63](https://user-images.githubusercontent.com/55113204/117576884-28517a00-b0f0-11eb-9bef-ce64e518639a.PNG)

![wire64](https://user-images.githubusercontent.com/55113204/117576886-28517a00-b0f0-11eb-9607-9859d28d9b8b.PNG)

![wire65](https://user-images.githubusercontent.com/55113204/117576887-28ea1080-b0f0-11eb-9702-645a8aef9b27.PNG)

![wire61](https://user-images.githubusercontent.com/55113204/117576888-28ea1080-b0f0-11eb-9807-70759c8097fb.PNG)

![wire62](https://user-images.githubusercontent.com/55113204/117576889-2982a700-b0f0-11eb-9b01-0c768bb07016.PNG)

## TCP İçin Kullanılabilecek Filtreler
![wire68](https://user-images.githubusercontent.com/55113204/117576967-7e262200-b0f0-11eb-82ad-34b91d54d82b.PNG)

![wire69](https://user-images.githubusercontent.com/55113204/117576968-7ebeb880-b0f0-11eb-99c0-073f30ed4a94.PNG)

![wire66](https://user-images.githubusercontent.com/55113204/117576969-7f574f00-b0f0-11eb-9ea5-21d19793f548.PNG)

![wire67](https://user-images.githubusercontent.com/55113204/117576970-7f574f00-b0f0-11eb-8e2e-3a1bdfc70d9f.PNG)

## FTP İçin Kullanılabilecek Filtreler
![wire72](https://user-images.githubusercontent.com/55113204/117577071-e8d75d80-b0f0-11eb-86b0-be142d9b5eb0.PNG)

![wire73](https://user-images.githubusercontent.com/55113204/117577072-e96ff400-b0f0-11eb-9fe3-4f5ead8fbba9.PNG)

![wire74](https://user-images.githubusercontent.com/55113204/117577073-e96ff400-b0f0-11eb-837b-fe2b28ed2c29.PNG)

![wire70](https://user-images.githubusercontent.com/55113204/117577074-e96ff400-b0f0-11eb-8e77-ee47a861c0d9.PNG)

![wire71](https://user-images.githubusercontent.com/55113204/117577075-ea088a80-b0f0-11eb-9cfd-333d21a9d26e.PNG)

## ICMP İçin Kullanılabilecek Filtreler
![wire76](https://user-images.githubusercontent.com/55113204/117577118-276d1800-b0f1-11eb-8105-baa5bd43a025.PNG)

![wire75](https://user-images.githubusercontent.com/55113204/117577119-2805ae80-b0f1-11eb-88ea-d8b95c343bb6.PNG)
















