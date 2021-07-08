## HANNAH VULNHUB WALKTHROUGH

Selam bugün yine vir makine çözümü gerçekleştirelim ister misiniz? O zaman biran önce başlayalım.

İlk önce her zamanki gibi makinemizin ip adresini öğrenelim. Ben bunun için netdiscover aracını kullanacağım.

![hannah](https://user-images.githubusercontent.com/55113204/124957883-3b19f980-e022-11eb-851d-e03fa35e8dd6.PNG)

Öğrendiğim ip adresi ile nmap aracını kullanarak port, işletim sistemi ve servis taraması gerçekleştireceğim.

![hannah1](https://user-images.githubusercontent.com/55113204/124957973-5422aa80-e022-11eb-968d-dc9b3b81c92e.PNG)

ftp yi kurcalayalım ve Anonymous name kullanarak passwordu da enterlayarak geçelim.Bunun sebebi Zenmap taramsıda yaptım ve name Anonymous göründü. Bazen parola vermiyorlar
şansımızı deneyelim bakalım.

![hannah2](https://user-images.githubusercontent.com/55113204/124987135-2c910980-e045-11eb-87fe-0e0a43d897ec.PNG)

Şimdi bakalım ftpnin altında bişey var mı? Yoksa gizli dizin araması ile bakalım.

![hannah3](https://user-images.githubusercontent.com/55113204/124987268-55190380-e045-11eb-8a5f-75088fd9116e.PNG)

Tamamdır .hannah girdik ve onun içine baktık karşımıza id_rsa diye bir dosya çıktı. Başka gizli dosya var mı diye dir -a ile de kontrol edebiliriz ve görünen o ki yok.

![hannah4](https://user-images.githubusercontent.com/55113204/124987781-e7b9a280-e045-11eb-82e2-02573fb87e28.PNG)

Daha sonra bu id_rsa yı get komutu ile kendi makinemize çekelim.

![hannah5](https://user-images.githubusercontent.com/55113204/124987944-12a3f680-e046-11eb-99b5-47e8fcd560e1.PNG)


Bu indirdiğimiz id_rsa nın korunması olmadığı için ona korumak vermek amacıyla yetki yükseltelim.

![hannah7](https://user-images.githubusercontent.com/55113204/124989289-acb86e80-e047-11eb-9cc6-3be81a958f75.PNG)

Şimdi düşünmek gerekirse key var, ssh bağlantısı için 61000 portuaçık ve hannah ismimiz var ve ise ssh bağlantısını kurabiliriz. -i parametresi ile çekilmiş şifreler girmek için
kullanılır. Daha sonra yolunu vermekteyiz.

![hannah6](https://user-images.githubusercontent.com/55113204/124989387-c063d500-e047-11eb-8a98-d15bdb43a0db.PNG)

İçerdeyiz. Bakalım neler varmış içerisinde.

![hannah8](https://user-images.githubusercontent.com/55113204/124990012-7af3d780-e048-11eb-9df8-6cc7d27733d0.PNG)

Evet ilk bayrağı aldık. 

Şimdiki hedef yetki yükseltme. İlk önce nerelerde ne yetkisi var onlara bakalım bunun için farklı bir kod olarak sadece permissionları getiren kodu kullanacağım.

![hannah9](https://user-images.githubusercontent.com/55113204/124990630-4cc2c780-e049-11eb-8ec9-ace08146bd97.PNG)

Şimdi bu çıktılar ile root yetkisi alabilmek için GTFOBins sitesine gidelim.

![hannah10](https://user-images.githubusercontent.com/55113204/124991656-9b249600-e04a-11eb-9821-ced3115985a7.PNG)

Bir tmp dosyası oluşturalım sebebi ise veriler ile ilgili çalışma yapılabilmesi için en iyi yer burasıdır. Daha sonra yetkilendirme vermek için bir kaç tane kod yazalım.

![hannah11](https://user-images.githubusercontent.com/55113204/124992621-e2f7ed00-e04b-11eb-8db9-f3505b9be456.PNG)

İşte oldu artık rootuz. Ve root.txt içindeki flagi de almış bulunuyoruz :)

![hannah12](https://user-images.githubusercontent.com/55113204/124993141-9d87ef80-e04c-11eb-9131-42565797a50c.PNG)

Şimdilik bu kadar :/ Başka makinelerde görüşmek üzereee :D



**¯\\\_(ツ)\_/¯**



















