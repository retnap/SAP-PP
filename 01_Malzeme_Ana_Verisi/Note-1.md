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



