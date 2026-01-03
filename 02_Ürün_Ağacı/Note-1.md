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

# :ledger: Alternatif Ürün Ağacı 

+ Bir malzeme için temel bir ürün ağacı oluşturulduktan sonra farklı bileşenler ile üretilebilme şansı varsa **alternatif ürün ağacı** tanımlanır.

+ Bu durumda, sistem alternatif ürün ağacı numarası ile aynı malzeme için birden çok ürün ağacı tanımlanmasına izin vermektedir.

+ **Üretim versiyonu** aracılığı ile alternatif ürün ağaçları arası seçim sağlanabilmektedir.

+ Aynı malzeme için birden fazla ürün ağacı mevcut ise ürün ağacı dahili numarası aynı kalmakta ve alternatif ürün ağacı numarası artırılmaktadır.

## :mag: Bileşen Verileri 

| Alan Adı | Kullanım | Değer | 
| :--- | :--- | :--- | 
| Kalem numarası | Görüntüde sıralama için serbestçe seçilebilir numaradır. | | 
| Bileşen | Ürün ağacını oluşturan bileşen malzemeler girilir. | |
| Kalem tipi | Kalemin türünü ve kullanılabilirliğini belirler. <br> Değerli ve stoksal takip yapılan bir malzeme için 'L' seçilir. | **C:** Planlama öğesi <br> **D:** Döküman kalemi <br> **I:** BO yapısı öğesi <br> **K:** Sınıf kalmei <br> **L:** Stok kalemi <br> **M:** Fantom malzeme <br> **N:** Depolanmayan malzeme kalemi <br> **R:** Değişken ölçülü kalem <br> **T:** Metin kalemi | 
| Kalem tanıtıcısı | Ürün ağacı kalemine tanıtıcı bir numara tayin edilir. Sistem tarafından otomatik verilir. | | 
| Sıralama ölçütü | Ürün ağacı kalemine tanımlayıcı bir değişken tanımlanır. | |
| Alt. kalem gös. | Ürün ağacı bileşeni için alt kalemlerin tanımlı olduğunu belirtir. | |

<br>

+ Her ürün ağacı kaleminin, tayin edildiği bir **kalem tipi** olmalıdır.
  + Bu kalem tipi, kalemin niteliklerini ve işlevlerini belirler.
  + Kalem tipi, bir malzeme için malzeme numarasının zorunlu, isteğe bağlı ya da izin verilmiş olup olmadığını kontrol etmektedir.
  + Stok kalemi seçilmiş ise bir malzeme ana verisi bulunmalıdır.
  + **L-Stok Kalemi:** Stok kalemi, bileşenin stok yöntemiyle takip edilen bir malzeme olduğunu belirtir. Aynı zamanda bu kalem tipi alt kalem tanımlanmasına izin verir.
  + **N-Depolanmayan malzeme kalemi:** Depolanmayan malzeme kalemleri hem malzeme ana verileri ile hem de malzeme ana verileri olmadan oluşturulabilmektedir.
  + Kalem tipi tanımlamak için **OS13** işlem kodu kullanılmaktadır.
  + **(+)** zorunlu giriş, **(.)** isteğe bağlı giriş, **(-)** bu kalem tipi için desteklenmez, **(x)** bu kalem tipi için desteklenir, **()** bu kalem tipi için desteklenmez anlamlarına gelmektedir.
 
<br>

## :mag: Ürün Ağacı Kalem Verileri - Miktar Verileri 

+ Bir üretim siparişi için bileşen gereksinimi aşağıdaki formül kullanılarak hesaplanmaktadır:

+ *Bileşen gereksinimi (ihtiyaç miktarı) = sipariş miktarı x bileşen miktarı / taban miktar*

| Alan Adı | Kullanım | Değer | 
| :--- | :--- | :--- | 
| Bileşen miktarı | Taban miktar bazında ürün ağacı bileşenin ihtiyaç miktarı girilir. | | 
| Bileşen ölçü birimi | Temel ölçü birimi x, ürün ağacı ölçü birimi y ise depolama veya iş planı görünümünde çıkış ölçü birimi y olarak tanımlanır ve dönüşüm oranı tanımlandıktan sonra ürün ağacına y girilir. | | 
| Net ıskarta göstergesi | Iskartanın, net ihtiyaç hesaplamasına göre hesaplanmasını sağlar. <br> (Başlık malzemesinin ana verisinden devralınan ıskarta oranını dikkate almaksızın) | |
| İşlem ıskartası (%) | Bileşenin, işlem gördüğü operasyon için ıskarta oranıdır. | | 
| Bileşen ıskartası (%) | Malzeme, bileşen olarak kullanıldığında öngörülen ıskarta oranıdır. | |
| Sabit miktar | Ürün ağacı bileşen miktarının başlık malzeme miktarından bağımsız olmasını sağlar. | |

<br> 

+ Belirli bir ürün ağacı için temel ölçü birimi geçersiz kılınabilir. Bunun için malzeme ana verisinde **çıkış ölçü birimi** kullanılır.

+ **Sabit miktar** örneğin 50 kg bir ürün üretmek için gerekli bileşen miktarı 50 kg olarak tanımlansın. Sistem ana ürünün üretim miktarı 35 kg olsa bile gerekli bileşen miktarını 50 kg olarak hesaplar.

+ **Yan ürün**, örneğin bir masa üretimi için talaş üretilebilmektedir. Talaşı ek bir bileşen (yan ürün) olarak ekleyebilir ve miktar alanına negatif bir değer alabilir.

+ **Yapay bileşen grubu (fantom)**, yapay kalem, stokta fiilen var olmayan ürün ağacındaki bir bileşen malzemedir. Ürün ağacını basitleştirmek için kullanılır.

## :mag: Ürün Ağacı Kalem Verileri - Genel Veriler 

| Alan Adı | Kullanım | Değer | 
| :--- | :--- | :--- | 
| Eş ürün | Üretim süreçleri sonucunda birden çok malzeme üretildiği durumda eş ürün tanımlaması yapılır. | | 
| Alternatif kalem grubu | Ürün ağacı içinde birbirinin alternatifi olacak bileşen malzemeler var ise bu malzemeler aynı alternatif kalem grubuna atanır ve kullanım yüzdesi girilir. | |
| Kesinti verileri | Malzemenin kesintiye uğrayacağını ve bir başka bileşen ile değiştirilebilirliğini kontrol eder. | | 
| Özyineleme odaklı | Özyineleme kontrolü yapılamayacak ise işaretlenir. | | 
| Özyineli | Ürün ağacının özyineli olduğunu gösterir. | |
| CAD göstergesi | Montaj veya bileşen malzemelerinin CAD çizimi sonucunda sisteme aktarıldığını gösterir. | |
| ALE göstergesi | Montaj veya bileşen malzemelerinin ALE ile bir başka sisteme dağıtımı yapıldığını gösterir. | | 
| Referans yer | Ürün ağacı bileşeni ve proje sistemi aktivitesi arasında referans yer tanımlanır. | | 


## :mag: Ürün Ağacı Açılımı 

+ Ürün veya ürün yapısının karmaşıklığına bağlı olarak birçok ürün ağacı düzeyi olabilmektedir.

+ Tüm bileşen listesinin elde edilmesi için **CS11/CS12** işlem kodları kullanılmaktadır.

## :mag: Ürün Ağacı Kullanım Yeri Listesi 

+ Ürün ağaçlarında bileşen olarak geçen bir malzemenin hangi ürünlerde kullanıldığı bilgisine ulaşmak gerekebilir.

+ Ürün ağacının kullanım yeri listesine **CS15** işlem kodundan ulaşılabilir.

## :mag: Ürün Ağacı Toplu Değişiklik Yapma 

+ Ürün ağaçlarında toplu değişiklikleri herhangi yeni bir gereksinimi karşılamak için yapılabilmektedir.

+ Ürün ağaçlarında toplu değişiklikleri yapmak için **CS20** işlem kodu kullanılmaktadır.

## :mag: Ürün Ağacı Değişiklikleri 

+ Bir ürün ağacında kalem ekler veya kaldırılırsa ya da mevcut kalemlerin miktarı güncellenirse; sistem değişiklik belgerinde yapılan bu değişikliği tutar.

+ **Ürün ağacında yapılan değişikliklerin görüntülenmesi** için; **CS80** işlem kodu kullanılmaktadır.

## :mag: MİP Düzeyi Kodu 

+ MİP alt düzey kodu, tüm ürün yapıları dahilinde bir malzemenin, içinde yer aldığı en alt açılım düzeyidir.

+ MİP alt düzey kodlamasına göre planlanacak malzemelerin sırası ihtiyaç planlamasında belirtilir.

+ MİP alt düzey kodlaması, en alt açılım düzeyindeki bir malzemeye ilişkin tüm ihtiyacı bir araya getirir ve malzemelerin birden fazla üründe ve birden fazla üretim düzeyinde bulunmasını dikkate alır.

+ Her ürün ve ürünün bileşen grupları için SAP sisteminde ayrı birer tek kademeli malzeme **ürün ağacı** oluştu.

+ MİP alt düzey kodu, ürün ağacı bakımı sırasında otomatik olarak tayin edilir ve ihtiyaç planlamasıyla maliyet hesaplamasında kullanılır.

+ MİP alt düzey kodu, her malzeme için malzeme ana verilerinin yönetim verilerinde görüntülenebilir.

## :mag: Özyinele 

+ Eğer bir ürün, kendisiyle aynı malzeme numarasına sahip bir bileşen içeriyorsa **ürün ağacı yineleyicidir**.

+ Özyinelemeli bir ürün ağacı yaratılmak isteniyorsa özyineleme olanaklı göstergesi belirlenmelidir.

## :mag: Alternatif Bileşen (Kesinti Malzeme) 

+ Birbirine alternatif malzemeler olması durumunda alternatif bileşen olarak ürün ağaçlarında tanımlanmaktadır.

+ Alternatif bileşenler tanımlanırken **kullanım önceliği** belirtilir.

+ Ürün ağacı içerisinde birbirinin alternatifi olacak malzemeler aynı alternatif kalem grubuna atanır ve kullanım yüzdesi girilerek bu malzemelerin kullanım oranları ayarlanır. Böylece, stok durumuna göre alternatif hammadde otomatik belirlenecektir.


## :mag: Müşteri Siparişi Ürün Ağacı 

+ Ürün ağaçlarını müşteri siparişine özel olarak oluşturmak için **CS61** işlem kodu kullanılır.

+ Başlangıç ekranında malzemenin yanı sıra müşteri siparişi ve müşteri siparişinin kalem numarası da girilir.

+ Sistemde müşteri siparişi ürün ağaçları **KDST** tablosunda tutulmaktadır.

+ **CSKB** işlem kodu ile müşteri siparişine ilişkin ürün ağaçları tarayıcısı kullanılabilmektedir.

## :mag: Proje Ürün Ağacı 

+ Ürün ağaçlarını projeye **özel** olarak oluşturmak için **CS71** işlem kodu kullanılır.

+ Başlangıç ekranında malzemenin yanı sıra **PYP** ögesi de girilir.

+ Sistemde proje ürün ağaçları **PRST** tablosunda tutulmaktadır.

+ **CSPB Proje Ürün Ağacı** tarayıcısı sayesinde, ürün ağaçları liste halinde çekilebilmektedir.

 

















