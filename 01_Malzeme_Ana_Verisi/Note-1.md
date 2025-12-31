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

# Malzeme Ana Verileri - Master Data 

+ Malzeme ana verileri, bir şirketin malzemeye ilişkin bilgilerinin bulunduğu en önemli veri kaynağıdır.

+ Malzemelerin şirket içinde çeşitli kullanıcı departmanları tarafından kullanılması ve her departmanın farklı malzeme bilgileri saklaması nedeniyle, malzeme ana verileri kullanıcı departmanlarına göre gruplanmış alt bölümlerden oluşmuştur.

+ Tek bir görünümde yer alan veriler, birden çok organizasyon düzeyinde geçerli olabilir.

+ SAP sisteminde **malzeme** **MM01** işlem kodu ile yaratılır.


## Malzeme Ana Verisi - Sektör 

+ Malzemenin sektöre tayin edilmesi, ekranları, ekranlarla ilgili sonuçları ve ekranlardaki sektöre özgü alanların gösterilmesine yardımcı olur.

## Malzeme Ana Verisi - Malzeme Türü 

+ Malzeme türü, malzeme stoklarının nasıl yönetileceğini, miktar değişikliklerinin malzeme ana verilerinde mi yoksa değer değişiklikleri olarak mali muhasebedeki stok hesaplarında mı güncelleneceğini belirler.

+ Malzemenin oluşturulması ensasında alacağı pek çok değer, özellikle standart maliyet ve maliyetlendirme adımları malzemenin türü ile direkt ilişkilidir.

+ Malzeme türü ayrıca, malzemeler stoğa kaydedildiğinde ya da depodan çıktığında hangi hesapların etkileneceğini belirler.

+ **Malzeme türleri (SPRO)**, **OMS2** işlem kodundan tanımlanabilir.

## Malzeme Görünümleri 

+ Malzeme, tüm sistem içerisinde tek bir tanımlama içerir fakat organizasyon yapısı düzeyinde (örn. üretim yeri) farklı parametre değerlerine sahip olabilir.

+ Üretim planlama modülünün (PP) tanımladığı ve kullandığı malzeme görünümleri:
  + **MİP1**
  + **MİP2**
  + **MİP3**
  + **MİP4**
  + **İş Planlaması**
  + **Tahmin**

### Temel Veriler

+ Malzeme ana verisi temel veriler (1-2) görünümleri, malzemenin üst birimi (tüm şirketler) düzeyinde tanımlanır.

+ Bu veriler, malzemeyi tanımlayıcı veriler (hacim, ebat, ağırlık vb.) ve malzemeye ilişkin çeşitli kriterler (mal grubu, bölüm vb.) içermektedir. 

### Temel Ölçü Birimi 

+ Malzeme için bir **temel ölçü birimi** seçilir.

+ Bu ürün ağacı taban miktarının ölçü birimi olan, stokların tutulacağı ve maliyetlerin hesaplanacağı bir ölçü birimidir.

### Mal Grubu (Material Group) 

+ Malzemeleri benzer özelliklerine, kullanım amaçlarına veya tedarik türlerine göre gruplandırmak için kullanılır.

### Harici Mal Grubu (External Material Group) 

+ Şirket içi kullanılan "Mal Grubu" alanından bağımsız olarak, dış kaynaklı (genellikle tedarikçilerin veya uluslararası standartların) gruplandırma kodlarını girmek için kullanılır.

+ Tedarikçilerle ortak bir dil konuşmak veya malzemenizi uluslararası bir sınıflandırma koduna (örneğin ECLASS veya UNSPSC) göre etiketlemek istenildiğinde kullanılır.

### Eski Malzeme No (Old Material Number)

+ Şirketin SAP sistemine geçmeden önce kullandığı eski sistemdeki (legacy system) malzeme numarasının kaydedildiği alandır.

+ Özellikle sistem geçiş süreçlerinde (Go-live sonrası), kullanıcıların eski numaralarla arama yaparak malzemeyi bulmalarını kolaylaştırır. Tamamen bilgi amaçlıdır.

### Bölüm (Division)

+ Malzemenin ait olduğu ürün hattını veya iş birimini temsil eder.

+ SAP'nin **Satış ve Dağıtım (SD)** modülü ile doğrudan ilişkilidir.

+ Satış analizleri yapmak ve belirli bir ürün grubuna (bölüme) özel fiyatlandırma veya satış stratejileri belirlemek için kullanılır.

## MİP Görünümleri

+ MİP görünümü bir malzemenin tedarik şeklini, planlama yönetimini ve üretim süreci içinde bu malzemenin kontrol edilmesi için nasıl tanımlanacağını içerir.

+ Tedarik türü, malzemenin dışarıdan tedarik veya dahili üretilecek ya da her iki senaryonun mümkün olduğunu belirtir. 

+ Mip sorumlusu ile belirli bir malzeme için **planlama sorumlusu** tanımlanır.

+ Mip karakteristiği bir malzemenin talebe dayalı ya da tüketim bazlı (örn. yeniden sipariş seviyesi ile planlama) olarak planlamanın olup olmayacağını gösterir.

### MİP1 - Genel Veriler

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

### MİP1 - MİP Yöntemi 

| Alan Adı | Kullanım | Değer | 
| :--- | :--- | :--- |
| MİP Karakteristiği | Malzeme ihtiyaç planlamasının yapılıp yapılmayacağı, yapılacaksa da yönetimini (plana dayalı/tüketime dayalı) denetler. <br> **Plana dayalı planlama** yönteminde tahmin veya satış belgesine istinaden gerçekleşen bir üretim planına girdi ve çıktıların dikkate alındığı planlama yöntemidir. <br> **Tüketime dayalı planlama** yönteminde stok seviyesinin belirli bir düzeyin altına düştüğünde tedarik önerisinin bu seviyeye ulaşacak şekilde önerilmesi veya tamamen tahmin verisine dayalı olarak gerçekleştirebilmektedir. | **PD:** Plana Dayalı <br> **ND:** Mip Yok <br> **VM:** Otomatik yeniden sipariş seviyesi ile planlama <br> **VB:** Manuel yeniden sipariş seviyesi ile planlama <br> **VV:** Tahmine dayalı Mip | 
| MİP Sorumlusu | Planlama çalışmaları ve raporlamalarda kullanılmak üzere sorumlu kişiler tanımlanır. | 001: Person | 
| Yeniden sipariş seviyesi | MİP Karakteristiği tüketime dayalı olan malzemeler için tedarik önerisi oluşturulacak seviyeyi temsil eder. Eğer düşerse sistem malzemeyi bir sonraki planlama için işaretleyecektir. | |
| Sabitleme Süresi | MİP'in sabit olarak kabul edeceği aralıktır. | | 
| Planlama Sıklığı | Planlamanın ve siparişin hangi gün yapılacağını belirten alandır. | | 

---

### MİP1 - Parti Büyüklüğü Verileri 

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

### MİP2 - Tedarik 

+ MİP2 Görünümü genellikle malzemenin tedarik şeklini, terminlemeye etki eden değerleri ve emniyet stoğu ile ilgili parametreleri içerir.


















