# :ledger: İşyeri

+ SAP sisteminde işyerleri operasyonların yürütüldüğü kaynaklardır.

+ Sistem üzerinde makineler, makine grupları, üretim hatları, montaj hatları, çalışanlar ve çalışan grupları işyeri olarak tanımlanabilir.

+ İşyeri, üretim alanının içindeki münferit makineleri değil tüm üretim alanını veya üretim hattını temsil edebilir.

+ İşyerleri aynı zamanda **maliyet muhasebesi (CO)** modülü için maliyet merkezleridir.

+ İşyerleri, üretime ilişkin temel organizasyonel birimlerdir.
  + Burada aktiviteler gerçekleştirilir ve çizelgeleme, kapasite ve maliyet hesaplaması amaçlarıyla kullanılır.
 
+ İşyerleri **üretim seviyesinde** tanımlanan bir ana veridir.
  + Temel veriler, varsayılan değerler, kapasiteler, terminleme, maliyet hesaplaması, teknoloji görünümlerinden oluşur.
 
+ **CR01** işlem koduyla işyeri yaratılabilir.

---

## İşyeri - Temel Veriler 

+ Temel veriler tabında, altı olası standart değere bir tanım ve bir boyut tayin etmek için standart değer anahtarı kullanılabilir.

+ Tanım tayini, standart deeğr kaynaklı formül parametreleri aracılığıyla gerçekleştirilir.

| Alan Adı | Kullanım | Değer | 
| :--- | :--- | :--- |
| İşyeri numarası | İşyerinin sistemde tanımlandığı kodudur (8 karakterdir). | |
| İşyeri tanımı | İşyerini açıklayan bir tanımıdır. | |
| İşyeri türü | İşyerindeki ekran sırasını ve alan seçimini denetler. | **0001: Makine** <br> **0003: Personel** <br> **0007: Üretim Hattı** |
| Plan Kullanımı | İşyerinin hangi iş planı tiplerinde kullanılabileceğini belirler. | **001: Yalnızca iş planları** <br> **009: Tüm plan tipleri** | 
| Sorumlu | Aynı üretim departmanı içerisinde benzer operasyonel özellik taşıyan işyerlerini kontrol edebilen organizasyonel birimlerdir. | 
| Yer | Üretim yerindeki fiziksel alanı temsil eden yer tanımlaması girilir. | | 
| Üretim tedarik alanı | İçeriğinde depo yeri bilgisi taşır. <br> Üretim tedarik alanı sayesinde bileşenler ile ilgili depo yerinden tüketilir. | | 
| Teyit sonrası oto. çekme | Otomatik olarak bileşen tüketiminin karar verilmesi | | 
| Standart değer anahtarı | Formüllerde kullanılacak parametrelerin tayin edildiği yapılardır. <br> Farklı masrafları temsil eder. | | 
| Giriş kuralı | Standart değerin girilmesi ya da girilmemesi için uyarıları ya da hataları gösterir. <br> "Doğrulama yok" seçilebilir. | | 

## İşyeri - İşyeri Türü 

+ İşyerleri, işlevlerine göre belirli işyerleri türlerine tayin edilir.

+ İşyerleri için alan ve ekran seçimini, temel olarak işyeri türü kontrol eder.

+ **SPRO** -> Üretim -> Temel Veriler -> İşyeri -> Genel Veriler -> İşyeri türü yoluyla veya **OP40** işlem kodundan tanımlanabilir. 

---

# :ledger: Kapasite 

+ Kapasite ekranları, işyerindeki kullanılabilir kapasitenin nasıl hesaplandığını kontrol etmektedir.
  + Belirli bir görevi yerine getirmek için potansiyeli temsil etmektedir. 

+ Kapasite planlaması için her işyeri bazında kullanılabilir kapasitenin tanımlanması gerekmektedir.

+ SAP sisteminde kapasite varlığı tanımlaması ve kapasite planlama **zaman birimi** üzerinden yapılır, vardiya programı vasıtasıyla günlük kullanılabilir kapasite tanımlanabilir. 

+ 📌 SAP sisteminde kapasiteler, belirli bir süre içinde kişiler ve makineler tarafından sağlanabilir hizmet olarak tanımlanmaktadır.

+ Standart kapasite varlığı ile **kullanılabilir kapasite** tanımlanır.
  + İş planı operasyonlarında belirtilen parametrelere atanan değerler, kapasite gereksinimini belirlemek için bir temel olarak hizmet vermektedir.
  + İşyeri kapasite görünümüne tayin edilen formüller, iş planındaki parametre miktarlarını esas alarak **kapasite gereksinimini** hesaplamaktadır.
 
+ Kapasite, genellikle direkt **işyeri üzerinden tanımlanır**.
  + İşyeri oluşturulduğu sırada kapasite türü girilerek **kapasite tanımlanması** başlatılır.
 
| Alan Adı | Kullanım | Değer | 
| :--- | :--- | :--- |
| Planlama grubu | Kapasitenin planlanmasından sorumlu grup | **001: SAP örneği** <br> **A: Planlama grubu A** | 
| Kapasite havuzu | Belirli bir makine grubu veya işçilik grubu kapasite havuzu oluşturulur. | | 
| Gruplama | Vardiya tanımları ve vardiya programlarının toplandığı genel bir gruplama tanımlanır. Böylece, bu grup altındaki vardiya tanımlamaları kullanılabilir. | |
| Fabrika takvimi tn. | Fabrikanın çalışma günlerini belirler. | TR |
| Etkin versiyon | Versiyonlar bazında farklı standart kapasite varlıkları tanımlanabilir. <br> Etkin versiyonun hangi kapasite versiyonu ile çalışacağı belirtilir. | **01: Normal kapasite vr.** <br> **02: Asgari kapasite vr.** <br> **03: Azami kapasite vr.**|
| Temel ölçü birimi | Kapasite ihtiyacının tanımlanacağı temel ölçü birimidir. | | 
| Başlangıç | Standart kapasite varlığı tanımlanmasında kapasite başlangıç saati | |
| Son | Standart kapasite varlığı tanımlanmasında kapasite bitiş saati | |
| Mola süresi | Standart kapasite varlığı tanımlanmasında kapasitedeki toplam mola saati | |
| Kullanım derecesi | Kapasitenin teorik ile gerçek kapasitesi arasındaki kullanım derecesidir. Verimlilik. | |
| Münferit. kpst. sayısı | Kapasite 5 ayrı makinesinden oluşuyor ise münferit kapasite sayısı 5 girilir. | |
| Kapasite terminleme ilişikili | Kapasite terminlemede geçerli olacak ise işaretlenir. | | 

<br> 

📌 **Standart kapasite varlığı**, kullanılabilir kapasitenin çalışma saati cinsinden hesaplanmasını sağlayan değerleri saklar. Aşağıdaki formüle göre hesaplanır:

ℹ️ Kullanılabilir kapasite = Kullanım süresi (Son-Başlangıç-Mola Süresi) x Münferit Kapasite Sayısı x Kullanım Derecesi / 100 

+ **OP32** işlem kodundan **kapasite türü** tanımlanabilir.
















