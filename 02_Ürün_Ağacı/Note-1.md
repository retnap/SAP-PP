# :ledger: Ürün Ağacı 

+ SAP sisteminde ürün ağaçları bir ürünü oluşturan malzemeler ve bu malzemelerin kullanılma miktarlarını içeren malzeme listesi olarak tanımlanır.

+ Tasarım safhasının sonucunda bir tasarım çizimi, ürünü üretmek için gerekli olan parçaların listesi ortaya çıkmaktadır ve bu veriler sisteme ürün ağacı olarak tanımlanmaktadır.

+ **Ürün ağaçları**, bir mamul ya da yarı mamul için gereken bileşenlerin miktarının ve kod bilgisinin yer aldığı listedir.
  + Entegre malzeme yönetimi, üretim yöneltimi ve ürün maliyet hesaplaması açısından **temel öneme sahip ana verileri** içermektedir.
 
+ Ürün ağaçları, üretilen bir kalemi veya bileşen grubunu oluşturmak için gereken kalemleri temsil eden malzeme listeleri veya ürün yapılarını saklamak için kullanılır.

+ Standard masraf hesaplamalarında malzeme masraflarının temeli olarak bileşen miktarları kullanıldığı için **ürün ağacı verilerinin doğru olması çok önemlidir**.

+ Üretilen her malzeme için bir ürün ağacı sistemde tanımlanmalıdır.
  + Malzeme ihtiyaç planlaması ürün ağaçlarını ve bu ürün ağaçlarındaki kullanım miktarlarını dikkate alarak planlı sipariş ve satınalma taleplerinin hangi alt bileşenler için ne miktarda oluşturulması gerektiğini hesaplar.
 
## :mag: Ürün Ağacı Yapısı 

![urun-agaci-yapisi](https://github.com/user-attachments/assets/12615fbb-98e5-49cb-bdb2-322b5d27c743)

*Kaynak: https://mavvo.com.tr/blog/urun-agaci-nedir/* 

## :mag: Ürün Ağacı Tipleri 

+ Ürün ağaçları şirket içerisinde farklı departmanlar tarafından farklı amaçlara yönelik oluşturulabilmektedir.

+ **Malzeme ürün ağaçları**, işletmede üretilen ürünlerin yapısını göstermek için kullanılır. (**İşlem kodu: CS01**)

+ **Müşteri siparişi ürün ağaçları**, bir ürünü özel bir müşteri siparişi için üretmekte kullanılır. (**İşlem kodu: CS61**) 

+ **Proje ürün ağacı**, proje sisteminde bileşenlerin girilmesine yardımcı olur. (**İşlem kodu: CS71**)

+ **Döküman ürün ağacı**, bir doküman bilgi kaydına girilir ve ağacı olarak tanımlanır. Bir döküman, birden fazla dökümandan oluşabilir, örneğin teknik çizimler, fotoğraflar, metinler vb. (**İşlem kodu: CV11**)

+ **Ekipman ürün ağaçları**, işletmede kullanılan makinelerin, ekipmanların vb. yapısını tanımlamak ve bakım/onarım doğrultusunda yedek parçaların ekipmana tayini için PM modülünde kullanılır. (**İşlem kodu: IB01**)

+ **Teknik birim ürün ağaçları**, ekipmanları belirli teknik birimlere bağlamak için PM modülünde kullanılır. (**İşlem kodu: IB11**)

---

## :mag: Ürün Ağacı Yapısı 

+ **Malzeme ürün ağacı**, **CS01** işlem kodu ile oluşturulmaktadır.

+ Malzeme, üretim yeri, kullanım ve ürün geçerlilik başlangıç tarihi girilir.

## :mag: Ürün Ağacı Başlık Verileri

+ Ürün ağacı, bir başlık bölümü ve bir kalem bölümünden oluşmaktadır.
  + Başlık bölümünde üretim yeri tayini, geçerlilik süresi ve durumu (serbest veya üretim için kilitli) gibi bilgiler yer almaktadır.
 
+ **Geçerlilik başlangıcı**, bir ürün ağacının oluşturulması sırasında, ürün ağacının etkin olacağı zaman geçerlilik başlangıcı tarihi belirler.
  + Ürün ağacını, bir değişiklik numarası belirtimiyle oluşturulur ya da değiştirilirse sistem geçerlilik başlangıcını değişiklik ana kaydından kopyalar.
 
+ **Geçerlilik sonu**, bu tarihle ürün ağacı için zamansal geçerliliğin bitişi belirlenir.
  + Sistem bunu dinamik olarak belirler.
  + Varsayılan bir değer sisteme girilmiştir (31.12.9999).
 
+ Bir değişiklik numarası belirtimi ile ürün ağacındaki bir bileşen başka bir bileşenle değiştirilirse yeni bileşendeki geçerlilik başlangıcı ve eski bileşendeki geçerlilik sonu ile aynı tarih olacaktır. Sistem, bu değişikliği eski bileşenden yeni bileşene aynı gün saat 00.00'da yapacaktır.

+ Ürün ağacı başlığındaki alanların açıklamaları aşağıdaki tabloda verilmiştir:

| Alan Adı | Kullanım | Değer | 
| :--- | :--- | :--- | 
| Ürün ağacı numarası | Dahili olarak ürün ağacının numaralandırılması (ürün ağacı grubu). <br> Sistem tarafından otomatik olarak verilir. | | 
| Ürün ağacı kullanımı | İşletme ilişkili uygulama durumlarında önem taşıyan kalemlerin varsayılan değerlerini belirler. | **1:** Üretim <br> **2:** Tasarım <br> **3:** Genel <br> **4:** Bakım ve onarım <br> **5:** Satış ve dağıtım <br> **6:** Maliyet hesaplaması | 
| Alternatif ürün ağacı | Malzemenin aynı üretim yerinde birden çok ürün ağacı olması durumunda, ürün ağaçlarını birbirinden ayırt etmek için kullanılır. | | 
| Ürün ağacı durumu | Ürün ağacının belli amaçlarla kullanılabileceğini ve tarihçe zorunluluğunu denetler. | **1:** Etkin <br> **2:** Etkin değil <br> **3:** Tarihçe yükümlülüğü ile etkin | 
| Taban miktar | Kalemdeki bileşen miktarı verilerinin referansta bulunduğu ürün miktarını gösterir. | | 
| ÜA metni | Ürün ağacını tanımlayan kısa metin girilir. | | 
| Alt. Mtn. | Alternatif ürün ağacı tanımlayan kısa metin girilir. | | 

--- 

## :mag: Ürün Ağacı Kullanımı 
















