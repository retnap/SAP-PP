# Üretim Yöntemleri 

## 1. Kesikli Üretim (Discrete Manufacturing)

+ Bu yöntemde ürünler **ayrı birer birim** olarak üretilir.

+ Üretim süreci parçalıdır ve genellikle düşük hacimli ancak **kompleks ürünler** için kullanılır.

+ **Üretim siparişi temelli** bir üretim yöntemidir.

+ Üretilen ürünlerde sıkça değişim gözlenebilir.

+ Ürünler sayılabilir (örn. 5 araba, 10 telefon) ve düzensiz taleplere göre üretim hattı hızlıca ayarlanabilir.

+ Örn: Mobilya, beyaz eşya, otomobil montajı, akıllı telefonlar ve uçak üretimi


## 2. Seri Üretim (Mass Production)

+ Aynı standarttaki ürünlerin, **çok yüksek miktarlarda ve kesintisiz** bir şekilde üretilmesidir.

+ **Zaman aralığı** veya **miktar** tabanlı bir üretim yöntemidir.

+ Verimlilik çok yüksektir ve birim maliyet çok düşüktür.

+ Maliyet dönem veya malzeme bazlı toplanır.

+ Örn: Konserve yiyecekler, plastik eşyalar, seri üretim tekstil ürünleri


## 3. Proses Üretim (Process Manufacturing)

+ Üretim, belirli bir formüle veya reçeteye dayanarak, hammaddelerin **kimyasal veya fiziksel değişimlere** uğratılmasıyla gerçekleşir.

+ Üretim başladıktan sonra geri dönüş zordur ve çıktı genellikle bir "birim" değil, hacim veya ağırlıktır.

+ Üretim akışı 7/24 kesintisiz olabilir.

+ Ürünler genellikle sıvı, gaz, toz veya granül formundadır.

+ Örn: Petrol rafineleri, ilaç üretimi, boya ve kimya endüstrisi 

---

# Üretim Stratejileri 

![mto_vs_mts](https://github.com/user-attachments/assets/533f5bc1-9f34-4c6e-8e81-c3375a9a5fe0)
*Kaynak: https://blog.megaventory.com/2023/05/make-to-order-vs-make-to-stock-a-comparative-study/*

## 1. Make to Stock (MTS) - Stoktan Üretim 

+ Bu stratejide ürünler, gelecekteki talepler tahmin edilerek (forecast) önceden üretilir ve depolanır. Müşteri ürünü almak istediğinde, ürün rafta hazırdır.

  + Talep tahminleri ve geçmiş satış verilerini baz alır.
 
  + Teslim süresi çok kısadır (hazır stoktan gönderim). Seri üretim sayesinde birim maliyet düşüktür.
 
  + Yanlış tahminler sonucunda elde fazla stok kalması (ölü stok) veya talebin karşılanmaması riski vardır.
 
  + Örn: Diş macunu, konserve ve yiyecekler, tekstil ürünleri, seri üretim ev aletleri

## 2. Make to Order (MTO) - Siparişe Göre Üretim 

+ Bu stratejide üretim, ancak kesin bir müşteri siparişi alındıktan sonra başlar. Ürün genellikle müşterinin özel isteklerine göre şekillendirilebilir.

  + Doğrudan gelen müşteri siparişine göre tetiklenir.
 
  + Stok maliyetleri minimumdur. Müşteriye özel ürün sunma imkanı sağlar ve ürünün elde kalma riski yoktur.
 
  + Teslim süresi uzundur (üretim süreci beklenir). Üretim maliyetleri genellikle daha yüksektir.
 
  + Örn: Özel tasarım mobilyalar, terzi dikimi takım elbiseler, lüks yatlar, özel endüstriyel makineler
 
## Özet Karşılaştırma Tablosu 

| Özellik | Make to Stock (MTS) | Make to Order (MTO) | 
| --- | --- | --- |
| **Üretim Zamanı** | Siparişten önce | Siparişten sonra | 
| **Teslim Süresi** | Çok kısa (hemen teslim) | Uzun (üretim süresi dahil) | 
| **Ürün Çeşidi** | Standart | Özelleştirilebilir / Özel | 
| **Stok Riski** | Yüksek (Elde Kalabilir) | Düşük (Sadece hammadde) | 

---

# :medal_sports: Malzeme Ana Verileri - Master Data 

+ Malzeme ana verileri, bir şirketin malzemeye ilişkin bilgilerinin bulunduğu en önemli veri kaynağıdır.

+ Malzemelerin şirket içinde çeşitli kullanıcı departmanları tarafından kullanılması ve her departmanın farklı malzeme bilgileri saklaması nedeniyle, malzeme ana verileri kullanıcı departmanlarına göre gruplanmış alt bölümlerden oluşmuştur.

+ Tek bir görünümde yer alan veriler, birden çok organizasyon düzeyinde geçerli olabilir.

+ SAP sisteminde **malzeme** **MM01** işlem kodu ile yaratılır.


## :ledger: Malzeme Ana Verisi - Sektör 

+ Malzemenin sektöre tayin edilmesi, ekranları, ekranlarla ilgili sonuçları ve ekranlardaki sektöre özgü alanların gösterilmesine yardımcı olur.

## :ledger: Malzeme Ana Verisi - Malzeme Türü 

+ Malzeme türü, malzeme stoklarının nasıl yönetileceğini, miktar değişikliklerinin malzeme ana verilerinde mi yoksa değer değişiklikleri olarak mali muhasebedeki stok hesaplarında mı güncelleneceğini belirler.

+ Malzemenin oluşturulması ensasında alacağı pek çok değer, özellikle standart maliyet ve maliyetlendirme adımları malzemenin türü ile direkt ilişkilidir.

+ Malzeme türü ayrıca, malzemeler stoğa kaydedildiğinde ya da depodan çıktığında hangi hesapların etkileneceğini belirler.

+ **Malzeme türleri (SPRO)**, **OMS2** işlem kodundan tanımlanabilir.

## :ledger: Malzeme Görünümleri 

+ Malzeme, tüm sistem içerisinde tek bir tanımlama içerir fakat organizasyon yapısı düzeyinde (örn. üretim yeri) farklı parametre değerlerine sahip olabilir.

+ Üretim planlama modülünün (PP) tanımladığı ve kullandığı malzeme görünümleri:
  + **MİP1**
  + **MİP2**
  + **MİP3**
  + **MİP4**
  + **İş Planlaması**
  + **Tahmin**

### :mag: Temel Veriler

+ Malzeme ana verisi temel veriler (1-2) görünümleri, malzemenin üst birimi (tüm şirketler) düzeyinde tanımlanır.

+ Bu veriler, malzemeyi tanımlayıcı veriler (hacim, ebat, ağırlık vb.) ve malzemeye ilişkin çeşitli kriterler (mal grubu, bölüm vb.) içermektedir. 

### :mag: Temel Ölçü Birimi 

+ Malzeme için bir **temel ölçü birimi** seçilir.

+ Bu ürün ağacı taban miktarının ölçü birimi olan, stokların tutulacağı ve maliyetlerin hesaplanacağı bir ölçü birimidir.

### :mag: Mal Grubu (Material Group) 

+ Malzemeleri benzer özelliklerine, kullanım amaçlarına veya tedarik türlerine göre gruplandırmak için kullanılır.

### :mag: Harici Mal Grubu (External Material Group) 

+ Şirket içi kullanılan "Mal Grubu" alanından bağımsız olarak, dış kaynaklı (genellikle tedarikçilerin veya uluslararası standartların) gruplandırma kodlarını girmek için kullanılır.

+ Tedarikçilerle ortak bir dil konuşmak veya malzemenizi uluslararası bir sınıflandırma koduna (örneğin ECLASS veya UNSPSC) göre etiketlemek istenildiğinde kullanılır.

### :mag: Eski Malzeme No (Old Material Number)

+ Şirketin SAP sistemine geçmeden önce kullandığı eski sistemdeki (legacy system) malzeme numarasının kaydedildiği alandır.

+ Özellikle sistem geçiş süreçlerinde (Go-live sonrası), kullanıcıların eski numaralarla arama yaparak malzemeyi bulmalarını kolaylaştırır. Tamamen bilgi amaçlıdır.

### :mag: Bölüm (Division)

+ Malzemenin ait olduğu ürün hattını veya iş birimini temsil eder.

+ SAP'nin **Satış ve Dağıtım (SD)** modülü ile doğrudan ilişkilidir.

+ Satış analizleri yapmak ve belirli bir ürün grubuna (bölüme) özel fiyatlandırma veya satış stratejileri belirlemek için kullanılır.

## :ledger: MİP Görünümleri

+ MİP görünümü bir malzemenin tedarik şeklini, planlama yönetimini ve üretim süreci içinde bu malzemenin kontrol edilmesi için nasıl tanımlanacağını içerir.

+ Tedarik türü, malzemenin dışarıdan tedarik veya dahili üretilecek ya da her iki senaryonun mümkün olduğunu belirtir. 

+ Mip sorumlusu ile belirli bir malzeme için **planlama sorumlusu** tanımlanır.

+ Mip karakteristiği bir malzemenin talebe dayalı ya da tüketim bazlı (örn. yeniden sipariş seviyesi ile planlama) olarak planlamanın olup olmayacağını gösterir.

### :mag: MİP1 - Genel Veriler

+ Malzeme ana verisi; MİP1 görünümü malzeme ihtiyaç planlama şeklini, parti büyüklüğünü, mip sorumlusu ve malzeme ihtiyaç planlamasına yön veren parametrelerin gruplandığı mip grubu verilerini içermektedir.

| Alan Adı | Kullanım | Değer |
| --- | --- | --- |
| Temel Ölçü Birimi | Malzemenin stok tutulan ölçü birimini temsil eder. | | 
| Satınalma grubu | Satınalma aktivitesini gerçekleştiren kişi veya grubu temsil eder. | | 
| Ü.Y'ye özgü mlz. durumu | Malzemenin kullanılabilirliğini sınırlamak üzere kullanılır. Satınalma, ürün ağacı, iş planı, üretim vb. ana veri ve işlevlerin kullanımı sınırlandırılır. | 01: Tedarik/Planlama için Bloke <br> 02: Tedarik/Planlama/Stok için Bloke | 
| MİP Grubu | Üretim planlaması ve malzeme planlamasına ilişkin değerlerin toplu halde tanımlandığı alandır. | 0000: Dışarıdan tedarik <br> 0001: Ön planlamasız dahili üretim <br> 0002: Ön planlamalı dahili üretim | 
| ABC göstergesi | Malzemeyi ABC analizine göre gruplandırmak için kullanılır. | A: Önemli malzeme <br> B: Orta derecede önemli malzeme <br> C: Önemi az olan malzeme | 
| ÜY. özgü mlz. durumu için gçrl. başlangıcı | Üretim yerine özgü malzeme durumu için geçerlilik başlangıç tarihi girilir |  | 

---

### :mag: MİP1 - MİP Yöntemi 

| Alan Adı | Kullanım | Değer | 
| :--- | :--- | :--- |
| MİP Karakteristiği | Malzeme ihtiyaç planlamasının yapılıp yapılmayacağı, yapılacaksa da yönetimini (plana dayalı/tüketime dayalı) denetler. <br> **Plana dayalı planlama** yönteminde tahmin veya satış belgesine istinaden gerçekleşen bir üretim planına girdi ve çıktıların dikkate alındığı planlama yöntemidir. <br> **Tüketime dayalı planlama** yönteminde stok seviyesinin belirli bir düzeyin altına düştüğünde tedarik önerisinin bu seviyeye ulaşacak şekilde önerilmesi veya tamamen tahmin verisine dayalı olarak gerçekleştirebilmektedir. | **PD:** Plana Dayalı <br> **ND:** Mip Yok <br> **VM:** Otomatik yeniden sipariş seviyesi ile planlama <br> **VB:** Manuel yeniden sipariş seviyesi ile planlama <br> **VV:** Tahmine dayalı Mip | 
| MİP Sorumlusu | Planlama çalışmaları ve raporlamalarda kullanılmak üzere sorumlu kişiler tanımlanır. | 001: Person | 
| Yeniden sipariş seviyesi | MİP Karakteristiği tüketime dayalı olan malzemeler için tedarik önerisi oluşturulacak seviyeyi temsil eder. Eğer düşerse sistem malzemeyi bir sonraki planlama için işaretleyecektir. | |
| Sabitleme Süresi | MİP'in sabit olarak kabul edeceği aralıktır. | | 
| Planlama Sıklığı | Planlamanın ve siparişin hangi gün yapılacağını belirten alandır. | | 

---

### :mag: MİP1 - Parti Büyüklüğü Verileri 

| Alan Adı | Kullanım | Değer |
| :---- | :---- | :--- |
| MİP Parti Büyüklüğü | Üretimi veya tedariği yapılacak malzemelerin parti büyüklüğünün nasıl hesaplanacağı tanımlanır. | **FX:** Sabit parti büyüklüğü <br> **EX:** İhtiyaca göre parti büyüklüğü <br> **WB:** Haftalık parti büyüklüğü <br> **MB:** Aylık parti büyüklüğü <br> **TB:** Günlük parti büyüklüğü <br> **PK:** Planlama takvimine göre parti büyüklüğü | 
| Sabit Parti Büyüklüğü | Malzemelerin her zaman belirli miktarda tedarik edildiği durumlarda kullanılır. | FX | 
| Asgari Parti Büyüklüğü | Tedarik önerisi miktarının minimum değerini belirtir. | | 
| Azami Parti Büyüklüğü | Tedarik önerisi miktarının azami değerini belirtir. Bu değerin üzerine çıkılmasına izin verilmez. |  | 
| Azami Stok | Bir malzemenini ulaşabileceği en fazla miktar olarak tanımlanır. | HB seviyesinde değer girilir. |
| Yuvarlama Değeri | Belirli miktar ve katlarında tedarik önerilerinin oluşturulmasını sağlar. | | 
| Yuvarlama Profili | Sipariş miktarlarını tedarik edilebilir miktarlara yuvarlamak için kullanılan alandır. | | 
| Bileşen Grubu Iskartası | Üretim esnasındaki montaj ıskartasını temsil eder. <br> Yüzde olarak tanımlanır ve üretilecek malzeme ile birlikte bileşen miktarını da artırır. | 
| Takt Zamanı | Birden çok tedarik önerisinin oluştuğu durumda, tedarik önerileri arası geçiş süresi olarak tanımlanır. <br> Malzeme ihtiyacı kapasite problemlerinden dolayı tek seferde karşılanamıyor ise tedarik aralığını gösteren alandır. | |
| Parti büyüklüğü sabit masrafı | MİP parti büyüklüğünde optimum parti büyüklüğü belirleme yöntemleri kullanılırsa girilecektir. <br> Sipariş oluşturma sabit maliyetidir. | | 
| Depo masrafları göstergesi | MİP parti büyüklüğünde optimum parti büyüklüğü belirleme yöntemleri kullanılırsa girilecektir. <br> Stok tutma maliyetinin belirlenmesinde kullanılır. | | 
| Ölçü birimleri grubu | Farklı ölçü birimlerinin gruplandığı alandır. | | 

---

### :mag: MİP2 - Tedarik 

+ MİP2 Görünümü genellikle malzemenin tedarik şeklini, terminlemeye etki eden değerleri ve emniyet stoğu ile ilgili parametreleri içerir.

| Alan | Kullanım | Değer | 
| :--- | :--- | :--- |
| Tedarik Türü | Malzemenin dahili mi üretileceği yoksa dışarıdan mı tedarik edileceği tanımlanır. | **E:** Dahili üretim <br> **F:** Dışarıdan tedarik <br> **():** Tedarik yok <br> **X:** Her iki tedarik türü de |
| Özel Tedarik | Malzemenin tedarik türünü daha detaylı olarak belirtmek için bu veri alanı kullanılır. Özel tedarik alanı, tedarik türü alanının etkinliğini kaldırır. | **10:** Konsinye <br> **20:** Dışarıdan tedarik <br> **30:** Fason üretim <br> **40:** Stok nakli <br> **50:** Yapay bileşen grubu <br> **52:** Doğrudan üretim / sipariş ağı <br> **60:** Yapay (ön planlama) <br> **70:** Başka üretim yerinden çekme <br> **80:** Başka üretim yerinde üretim |
| Kotalama kullanımı | Malzemenin hangi seviyelerinde (satınalma talebi, planlı sipariş vb.) kotalama kullanılacağının belirtildiği alandır. | | 
| Teyit sonrası otomatik çekme | Üretim gerçekleştirildiği (teyit verildiği sırada) kullanılan malzemelerin depolardan otomatik olarak çekilmesini (sarf edilmesini) sağlar. | **1:** Her zaman üretim sonrası otomatik çekme <br> **2:** Üretim sonrası otomatik çekme kararını iş yeri verir |
| Parti Girişi | Bileşenler için parti belirleme işleminin ne zaman yapılacağını gösteren alandır. <br> Üretim siparişi onay sırasında otomatik belirlenmesi sağlanabilmektedir. | **0:** Mal çıkışı sırasında parti, teyit gerekli değil <br> **1:** Sipariş onayı sırasında manuel parti belirleme gerekir <br> **2:** Üretim/proses siparişinde parti gerekli değil; teyit gerekir <br> **3:** Sipariş onayı sırasında değişen otomatik parti belirleme | 
| Üretim Depo Yeri | Bileşenler için malzemenin tüketiminin yapılacağı depo yeri, yarı mamul ve mamuller için üretilip depoya konulacağı depo yeri anlamına gelmektedir. |  | 
| Önerilan ÜTA | Malzemenin öncelikli olarak nereden tedarik edileceğinin belirttiği alandır. | | 
| Dışarıdan tedarik depo yeri | Dışarıdan tedarik edilen malzemelerin stok girişinin yapılacağı depo yeridir. | | 
| Stok belirleme grubu | Depo yerinin belirlenmesi için çeşitli kuralları içerir. | | 
| Eş Ürün | Üretim süreçleri sonucunda birden çok malzeme üretildiği durumda eş ürün tanımlaması yapılır. <br> Örn: A4 üretilirken kağıdın gerekli kısmı kullanıldı ve kalan kısmı da değerli bir ürün yapmak için kullanıldı. | | 
| Dökme Ürün | Net ihtiyaç planlaması dahil edilmeyen, planlaması tüketim esasına göre yapılan miktarı önemsiz malzemeler için tanımlanır. <br> Hiç bitmeyecekmiş gibi davranılır. | | 

--- 

### :mag: MİP2 - Terminleme 

| Alan | Kullanım | Değer | 
| :--- | :--- | :--- |
| Dahili Üretim Süresi | Bir malzemeyi üretmek için gereken süre tanımlanır. <br> Girilen süre üretim büyüklüğünden bağımsızdır. <br> Mip terminleme parametresi "1" seçilirse dikkate alınır. | | 
| Planlı teslimat süresi | Dışarıdan tedarik edilecek bir malzemenin iş günü üzerinden tedarik edileceği süredir. | | 
| MG işleme süresi | Malzeme tedarikinin planlanan bitiş süresinden, malzemenin kullanılabilir hale gelene kadarki süreyi temsil eder. <br> Örn: Malzeme 12 günde üretildi, aktif hale gelmesi için 2 gün daha lazım.| |
| Süre Anahtarı | Tampon zamanları belirlemek için girilen alandır. Kullanılabilecekler: <br> Açılış Süresi, <br> Emniyet Süresi, <br> Üretim Öncesi Tampon Zaman, <br> Onay Süresi. | Süre anahtarı '000' da herhangi bir tampon süre yoktur. | 
| Planlama takvimi | Planlamanın yapılması istenen dönemleri içeren takvim atanır. | Parti büyüklüğü - PK değeri seçilmişse kullanılır. | 

---

### :mag: MİP2 - Net İhtiyaç Planlaması 

| Alan Adı | Kullanım | Değer | 
| :--- | :--- | :--- | 
| Emniyet Stoğu | Depoda sürekli tutulmak istenen stok miktarıdır. | | 
| Asgari Emniyet Stoğu | Otomatik hesaplanan emniyet stoğunun altına düşülemeyeceği miktarıdır. | |
| İhtiyaç Ön Süresi | İhtiyaç ön süresinin sadece birincil ihtiyaçlar için mi tüm ihtiyaçlar için mi kullanılacağını belirleyen göstergedir. | | 
| İhtiyaç Ön Süresi (iş günü) | Malzemenin ihtiyaçlarının öne çekilmek istendiği gün sayısı girilir. | | 
| İhtiyaç Ön Süresi Dönem Profili | İhtiyaç ön süresi için başlangıç ve bitiş tarihlerini içeren profil tayin edilir. | |
| Teslim edilebilirlik derecesi (%) | Hizmet düzeyi olarak otomatik emniyet stoğu hesaplamasında dikkate alınır. Malzemenin ihtiyacının karşılanabilme yüzdesidir. | |
| Yeterlilik Profili | Dinamik olarak ihtiyaca göre emniyet stoğu hesaplanmasını sağlar. <br> Dinamik emniyet stoğu ortalama günlük ihtiyaçlar temel alınarak hesaplanan istatistiksel bir hesaplamadır. | | 

--- 

### :mag: MİP3 - Tahmini İhtiyaçlar 

+ MİP3 görünümü genellikle ön planlama stratejisi, mahsuplaşma tipi ve aralığı, kullanılabilirlik kontrolü parametrelerini içermektedir.

| Alan Adı | Kullanım | Değer | 
| :--- | :--- | :--- |
| Dönem göstergesi | Tüketim değerlerinin hangi dönem bölümlemesi ile güncelleneceğini belirler. | **M:** Aylık <br> **W:** Haftalık <br> **T:** Günlük | 
| Mali yıl varyantı | Mali yılı tanımlayan mali yıl varyantı girilir. <br> Mali yıl içerisinde ne kadar kayıt dönemi olacağı belirtilir. | | 
| Dağıtım Göstergesi | Tahmine dayalı mip yöntemi ve periyot uzunluğu 'Gün' olmayan tahminlerin nasıl dağıtılacağı belirtilir. | | 

---

### :mag: MİP3 - Ön Planlama 

| Alan Adı | Kullanım | Değer | 
| :--- | :--- | :--- |
| Strateji Grubu | Planlama stratejisini (sipariş üzerine üretim/stoğa üretim) belirtir. <br> Planlanmış ihtiyaçların ve müşteri ihtiyaçlarının mahsuplaşmasını denetler. <br> Firmanın üretim tipine, stok yapısına ve de satış politikasına uygun grup ya da gruplar seçilerek planlamaya ve üretime yön verilir. | **10:** Depoya Üretim <br> **11:** Depoya üretim/brüt planlama <br> **20:** Sipariş üzerine üretim <br> **30:** Parti büyüklüğüne göre üretim <br> **40:** Son montaj ile ön planlama <br> **50:** Son montajsız ön planlama <br> **81:** Üretim siparişleri ile montaj işlemleri | 
| Mahsuplaştırma Kipi | Hangi zaman aralığında planlı birincil ihtiyaçlar, satış siparişleri, ikincil ihtiyaçlar ve rezervasyonlar tarafından tüketileceğini belirler. | **1:** Yalnızca geriye dönük mahsuplaştırma <br> **2:** Geriye ve ileriye dönük mahsuplaştırma <br> **3:** Yalnızca ileriye dönük mahsuplaştırma <br> **4:** Geriye ve ileriye dönük mahsuplaştırma | 
| Tüketim arl. ileriye | Birincil ihtiyaçların ileriye doğru kaç günlük dönem içerisinde satış siparişlerine mahsuplaşacağı bilgisidir. |  | 
| Mhsp. arl. geriye | Birincil ihtiyaçların geriye doğru kaç günlük dönem içerisinde satış siparişlerine mahsuplaşacağı bilgisidir. | | 
| Karma MİP | Planlama stratejisinin brüt planlama ve son montajsız bileşen grubu ön planlaması olarak kullanılması durumunda kullanılacaktır. | **1:** Son montaj ile bileşen grubu ön planlaması <br> **2:** Brüt planlama <br> **3:** Son montajsız bileşen grubu ön planlaması | 
| Ön Planlama Malzemesi | Planlama malzemesi ile planlama stratejisi kullanıldığında geçerlidir. Malzemeye ait satış siparişi ön planlama malzemesinin ihtiyacını tüketmektedir. | | 
| Planlama Üretim Yeri | Planlama malzemesi ile planlama stratejisi kullanıldığında geçerlidir. Referans alınan malzemenin hangi üretim yerinden alındığını gösterir. | 
| Dönüştürme Faktörü | Malzemenin TÖB ile planlama malzemesinin ölçü birimi arasında dönüşümü sağlayan oran belirtilir. | | 
| Ön pln. mlz. temel öb. | Ön planlama malzemesinin ölçü birimi girilir. | | 

---

### :mag: MİP3 - Kullanılabilirlik Kontrolü 

| Alan Adı | Kullanım | Değer | 
| :--- | :--- | :--- |
| Kullanılabilirlik Kontrolü | Malzemenin kullanılabilir miktar hesabı yapılırken bu hesaplamaya hangi değerlerin (satınalma siparişi, rezervasyonlar vb.) dahil edileceğini ve hesaplamanın hangi ihtiyaçlara yönelik olduğunu belirler. | **01:** Günlük İhtiyaç <br> **02:** Münferit İhtiyaç <br> **KP:** Kontrol yok | 
| Toplam İkmal Süresi | Kullanılabilirlik kontrolünde dikkate alınacak süredir. <br> Malzemenin ne kadar zaman içinde tekrar kullanılabilir olduğunu belirtir.  | | 
| Projeler Arası Malzeme İçin Gösterge | Proje stok segmentinde hesap tanımlı olmasa bile stok hareketlerinin dikkate alınmasını sağlayan alandır. | | 

---

### :mag: MİP3 - ÜY'ye Özgü Konfigürasyon 

| Alan Adı | Kullanım | Değer | 
| :--- | :--- | :--- |
| Varyant | Malzemenin varyant malzeme olarak takip edildiğini belirtir. | | 
| Konfigüre Edilebilir Malzeme | Varyant malzemenin kullanacağı konfigürasyon alt yapısının, hangi konfigüre malzemeye ait olduğunun tayininin yapıldığı alandır. | | 

--- 

### MİP4 - Ürün Ağacı Açılımı / İkincil İhtiyaçlar 

+ MİP4 görünümü genellikle ürün ağacı/iş planı açılım şeklini, bağımlı ihtiyaçların aktarım şeklini (MTO/MTS), kesinti verilerini, seri üretim ve depo yeri ayrı planlaması durumunda tanımlanacak değerleri içermektedir.

| Alan Adı | Kullanım | Değer | 
| :--- | :--- | :--- |
| Alternatif Seçim | Alternatif ürün ağacı seçimlerinin MİP sırasında nasıl yapılacağı belirlenir. | **0:** Sipariş miktarına göre seçim <br> **1:** Açılım terminine göre seçim <br> **2:** Üretim versiyonuna göre seçim <br> **3:** Yalnızca üretim versiyonuna göre seçim | 
| Münferit/Toplu | MİP'teki ikincil ihtiyaçların işlenmesini denetler. <br> Sipariş üzerine üretim söz konusu olduğunda önem taşır. <br> Münferit seçildiğinde sistem, malzemeye olan ihtiyaçları ihtiyaç kaynağı bazında ayıracaktır. <br> Toplu seçildiğinde sistem, malzemeye belli bir periyotta ihtiyaç duyulan miktarları toplayacak ve toplu olarak gösterecektir. | **0:** Münferit ve toplu ihtiyaç <br> **1:** Yalnızca münferit ihtiyaç <br> **2:** Yalnızca toplu ihtiyaç | 
| İhtiyaç Gruplaması | Aynı güne düşen ikincil ihtiyaçların gruplanmasını sağlar. | **T:** İkincil ihtiyaçların günlük toplamlar halinde görüntülenmesi <br> **0:** Seri üretimde, toplam ihtiyaca ek olarak münferit ihtiyaç | 
| Bileşen Iskartası (%) | Ürünün ağacındaki bileşenin üretim sarf edildiğinde ne kadarının ıskarta olacağı belirtilen alandır. | | 
| Bağımlı ihyç. için MİP uyumlu | Bağımlı ihtiyaçların MİP 'e dahil olup olmadığını belirten alandır. | **0:** Bağlı ihtiyaçlar planlanıyor <br> **1:** Bağlı ihtiyaçlar planlaması | 
| Versiyon Göstergesi | Malzemenin üretim versiyonu tanımlı olduğunda otomatik olarak işaretlenir. | | 

--- 

### MİP4 - Kesinti Denetimi 

| Alan Adı | Kullanım | Değer | 
| :--- | :--- | :--- |
| Kesinti Göstergesi | Kesinti göstergesi konulan malzemelerde bu malzemenin yerine başka malzeme kullanılacağını gösterir. | **1:** Artık üretilmeyen tek/paralel ürün <br> **3:** Artık üretilemeyen bağlı paralel ürün | 
| Sonraki Malzeme | Kullanıma son verilen malzemenin yerine geçecek olan malzemenin numarası bu alana girilir. | | 
| Kesinti Tarihi | Malzeme kesin bir tarihten itibaren kullanılamayacaksa kesinti malzeme ile birlikte bu alan doldurulur. | | 

---

### MİP4 - Seri Üretim / Montaj / Yayılma Stratejisi 

| Alan Adı | Kullanım | Değer | 
| :--- | :--- | :--- |
| Seri Üretim | Malzemenin üretim stratejisinin seri üretim olacağını belirleyen göstergedir. | | 
| Seri Üretim Profili | Seri üretim için mali hareketleri, çekme hareketi ile ilgili parametreleri, maliyetlendirme stratejileri gibi değerlerin uyarlamasını içinde barındıran değerlerdir. | |
| İşlem Denetimi | Planlı siparişler için işlev denetimlerinin hangi sırayla gerçekleşeceği belirtilir. | | 
| Eşit Paylaşım Kuralı | Talebin tedarikleri aştığı durumda dağıtım kaynakları planlamasının adil dağıtım yapacağı mip ögeleri belirtilir. | | 
| Push Dağıtımı | Toplam tedarik ögelerinin ihtiyaçları karşıladıktan sonr artan stok için davranışı belirtilir. | | 
| Teklif Süresi | Dağıtım kaynaklarının planlamasında gün sayısı olarak dağıtım yapılacak miktarın hesaplanmasında kullanılır. | |
| Ortalama Üretim Yeri Stoğu | Uzun dönemli planlama için ortalam üretim yeri stoğunun hesaplanmasını sağlar. | | 

---

### MİP4 - Depo Yeri Planlaması 

| Alan Adı | Kullanım | Değer | 
| :--- | :--- | :--- |
| MİP Göstergesi | Depo yeri bazında ayrı malzeme ihtiyaç planlaması için kullanılır. | | 
| DY Özel Tedarik Türü | Depo yeri bazında özel tedarik türünün belirlendiği alandır. | |
| Yeniden Sipariş Seviyesi | Depo yeri bazında yeniden sipariş seviyesinin belirlendiği alandır. | | 
| İkmal Miktarı | Depo yeri bazında tedarik miktarının belirlendiği alandır. | | 

--- 


















