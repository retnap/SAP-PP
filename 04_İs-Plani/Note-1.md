# :ledger: İş Planı 

+ Bir ürünün üretilmesi sürecinde geçen operasyonların sıra ile belirtildiği, malzemelerin üretimini planlamayı ve imalatını mümkün kılan ana veridir.

+ İş planı operasyonlarında belirtilen değerler terminleme, kapasite gereksinimi ve maliyet hesaplarında temel olarak dikkate alınır.

+ **İş planı**, bir mamülün veya yarı mamül parçanın üretimine ilişkin üretim prosesini ve gerekli kaynakları tanımlayan bir dizi işlemdir.
  + Fabrika içinde belirli bir rotaya ilişkin farklı adımları ve iş akışlarını yansıtarak bir ürün oluşturmanın farklı yollarını temsil etmek için kullanılır.
 
+ İş planlarında genel olarak her bir operasyonun hangi işyerlerinde yapılacağı, operasyonların sırası ve standart değer parametrelerine miktar girişi tanımlanır.

+ Stok olarak takip edilmemesi ancak üretim miktarının takip edilmesi gereken yerlerde bir yarı mamül seviyesi tanımlanmadan operasyon tanımlanır ve bu operasyona **teyit noktası** tayin edilir.

+ İş planı genellikle **kesikli üretim tipinde** kullanılır.

+ Bir iş planı tanımlamak için **CA01** işlem kodu kullanılır.

+ İş planının içerdiği bilgiler özetle;
  + Bir malzemeyi imal etmek için adım adım gereken operasyonlar ve uygulanacak işlemlerin sıralaması,
  + Parti büyüklük aralığına göre farklı iş planı tanımlamaları,
  + Kullanım (üretim, yeniden işleme, prototip...),
  + Durum (yaratılıyor, onaylandı...) açısından bir normal iş planı yaratabilmesi,
  + Hazırlık ve işleme gibi faaliyetler için standart değerler (süreler),
  + İşlemlerin uygulandığı işyerleri,
  + İşlemlere tayin edilen malzeme bileşenleri,
  + İşlemi uygulmaya koymak için gerekli olan tüm üretim yardımcısı araçları,
  + Kontrollerin gerçekleştirildiği işlemler için kontrol karakteristikleri,
  + Her bir işlemde yapılacakları belirten talimatlar,
  + Alternatif sıra ile standart sıradaki işlemler yerine diğer işlemleri seçme olanağını sunar. Örneğin, bir makine kullanım dışı olduğunda alternatif bir sıra seçebilir,
  + Paralel sıra ile aynı anda farklı işlemlerin gerçekleştirilmesini olanaklı kılar.
 
## 🏤 Plan Tipleri 

+ Plan tipleri, çeşitli uygulamlara (PP-SFC, PP-REM, PP-PI, PP-SOP, PS, QM) tayin edilir.
  + Plan tipine göre (örneğin; N) sistem hangi plan tipinde hangi kullanımların gerçekleşebileceğini denetler.
 
| Plan Tipi | Gösterge | Uygulama |
| :--- | :--- | :--- |
| Normal İş Planı <br> Standart İş Planı | N <br> S | PP-SFC | 
| Üretim Hızı Planı <br> Standart Üretim Hızı Planı | R <br> M | PP-REM | 
| Planlama Reçetesi | 2 | PP-PI | 
| Kaba Planlama Profili | 3 | PP-SOP | 
| Standart ağ | 0 | PS |
| Kontrol planı | Q | QM | 

+ **Normal iş planı**, üretim planlamasında malzemeye dayalı üretimi tanımlar.

+ **Standart iş planı**, geniş ölçüde malzemeden bağımsızdır. Normal iş planları için referans ve örnek olarak kullanılaiblir.

+ **Üretim hızı planı**, bir üretim hattı dahilinde malzemeye dayalı üretimi tanımlar ve çoğunlukla seri üretimde kullanılır.

+ **Standart üretim hızı planı**, üretim hızı planlarının genel olarak (malzeme bağımsız) oluşturulmasına yardımcı olur.

+ **Planlama reçetesi**, proses tipi üretim (PP-PI) modelinde kullanılır.

+ **Kaba planlama profili**, satış ve üretim kaba planlaması uygulamasında kullanılır.

+ **Standart ağlar**, etkin ağ planlarının yaratılması için referans olarak kullanılabilen, projeden bağımsız ağ yapılarıdır.

+ **Kontrol planı**, kalite kontrol işlemleri için ve üretimle ilişkili işlemler dizisinin yürütülmesi için kullanılır. 

## 🏤 Plan Kullanımı 

+ Çeşitli iş alanlarına yönlendirmek amacıyla plan için kullanım belirtilir.

+ Bu nedenle, bir malzemenin üretimi için çeşitli kullanımlar (üretim, tasarım, genel vb.) ile iş planları oluşturulabilir.

+ **OP46** işlem kodu ile yeni bir plan kullanımı oluşturulabilir.

## 🏤 İş Planı - Başlık 

| Alan Adı | Kullanım | Değer |
| :--- | :--- | :--- |
| Plan grup numarası | Dahili olarak iş planının numaralanması (plan grubu) | | 
| Plan grubu sayacı | İş planı grubu numarası altında kaç farkı iş planı olduğunu tanımlar. | |
| Üretim yeri | İş planının tanımlandığı üretim yeridir. | |
| Üretim hattı hiyerarşisi | Üretim hattı tasarımında farklı segmentlere ait işyerlerinin hiyerarşik olarak en üst seviyesini temsil eder. | |
| Kullanım | Planın hangi işletme ilişkili amaçlar için kullanılacağını denetler. | **1:** Üretim <br> **2:** Tasarım <br> **3:** Genel <br> **4:** Bakım ve onarım <br> **5:** Mal girişi |
| Plan durumu | Planın hangi işlevler için kullanılabileceğini gösterir. | **1:** Yaratma evresi <br> **2:** Sipariş için onaylandı <br> **3:** Hesaplama için onaylandı <br> **4:** Genel olarak onaylandı | 
| Planlama grubu | Üretim yöneltiminde ve kapasite planlamasında sorumlu çalışan ya da grup tanımlanır. | | 
| Planlama yeri | Kapasite dengelemesi yapılırken planlı siparişler için "kritik işyeri" belirtilir. | |
| Parti büyüklüğü bşl. | Etkin iş planı belirlenirken parti büyüklüğünün başlangıç değeridir. | |
| Parti büyüklüğü bitişi | Etkin iş planı belirlenirken parti büyüklüğünün bitiş değeridir. | | 

+ **Kullanım: "1"** - Üretim için olduğunu işaret eder.
  + Bu kullanım üretim aktivitelerinin gerçekleştirilebilmesi için iş planının kullanılabilir olduğunu gösterir.  

+ **Durum: "4"** - Genel olarak onaylandı durumuna sahip olduğunu işaret eder.
  + Bu kullanım üretim aktivitelerinin gerçekleştirilebilmesi için iş planı durumunun kullanılabilir olduğunu gösterir.
 
📌 **Alternatif iş planı** oluşturulabilir. Plan grubu numarası aynı olmakta ve plan grubu sayacı artmaktadır. 

📌 Bir iş planına birden çok **malzeme** atanabilir. 

## 🏤 İş Planı - İşlem 

+ İş planı işlem bilgilerinde, üretim operasyonları ve sırası yer almaktadır.

+ Operasyonlar dahili üretim olarak gerçekleşecek ise işyerleri ve buna uygun **denetim anahtarları** tayin edilir.

| Alan Adı | Kullanım | Değer |
| :--- | :--- | :--- |
| İşlem numarası | İşlemleri işleme sırasını belirler. | |
| İşyeri | İşlemin yürütüldüğü işyeridir. | |
| Denetim anahtarı | İşleme bağlı iş akışlarını denetler. | **PP01:** Ara operasyon <br> **PP02:** Harici operasyon (fason) <br> **PP03:** Son operasyon (oto. mal girişi) | 
| Std. metin anahtarı | Operasyonlara otomatik olarak gelecek kısa tanımlamaları içerir. | |
| İşlem kısa metni | Operasyonu tanımlayan bir kısa metin girilir. | | 

## 🏤 Denetim Anahtarı 

+ Denetim anahtarı; teyit şeklini, terminleme ya da kapasite planlaması alakalı olup olmadığını belirlemek, otomatik mal girişi olup olmayacağını, işlemin harici (fason) olarak gerçekleşip gerçekleşmeyeceğini ve çeşitli parametreleri içerir.

+ **OP67, OP00, OPJ8** işlem kodları ile tanımlanabilir.

+ Denetim anahtarı ile belirlenen en temel özelliklerden biri **otomatik mal girişi** işaretidir.
  + İşaretlendiğinde (örneğin PP03) sistem teyit ile birlikte mal girişi hareketini birlikte gerçekleştirecektir.

📌 Bir iş planı operasyon sıralamasında, otomatik mal girişi denetim anahtarına sahip birden fazla operasyon var ise sistem herhangi bir mal girişi önermemektedir. 

+ Harici işleme terminlemesi işaretli ise planlı teslimat süresi dikkate alınmaz ve standart parametre değerleri ile termin süresi hesaplanır. 

## 🏤 Standart Değerler 

+ Standart değerler, iş planı için önemli bir bilgi olup operasyon taban miktarına bağlı olarak tanımlanır.

+ CA01/CA02 işlem kodları içerisinde sağ üstte bulunan buton rotalama yapılır.
  + Hazırlık süresi, makine süresi, işçilik süresi mutlaka girilir.
 
## 🏤 Sıra 

+ İş planı operasyon sırası doğrusal bir dizilim içermektedir ve bu dizilim iki farklı şekilde değiştirilebilir.
  + Paralel sıra ile bir siparişin belirli işlemleri aynı anda yapılabilir hale gelir.
  + Eğer üretim farklı bir alternatif dizilim şeklinde üretilebilir ise **alternatif sıra** tanımlanır.
  + İş planı içerisinde "sıralar" butonu ile tüm sıralar çağırılabilir.
 
+ Standart sıranın sıra türü **0**, Paralel sıranın **1** ve Alternatif sıranın **2** dir.

## 🏤 İş Planının Silinmesi 

+ Sistemde iş planına ait bir nesne olmadığı durumda direkt olarak silinebilmesi mümkündür.

+ Silme işlemi **CA98** işlem kodundan yapılabilir.

+ Silinecek malzeme ve üretim yeri belirlenir.
  + Plan tipi alanında normal iş planını temsil eden **"N"** ve veritabanından sil bölümünde **"Eksiksiz planlar"** seçilir.
  + Yürütmenin ardından yeni açılan pencerede etkilenecek planlar listelenir.
  + Planların seçimi ve devam ile birlikte planların veri tabanından silinmesi gerçekleşir.
 
## 🏤 Üretim Versiyonu 

+ Bir malzemenin iş planı ile ürün ağaçlarının farklı kombinasyonlarının tanımlandığı **ana veriler**dir.

+ Üretim versiyonları, belli bir ürüne yönelik çoklu üretim yöntemlerini tanımlamak için kullanılan isteğe bağlı bir ana veri ögesidir.

+ Bu üretim versiyonunu yaratırken bir **ürün ağacı** ve **iş planı bileşimi** tanımlanır ve gerekirse versiyona yönelik parti büyüklüğü veya geçerliliği de tanımlanabilir.

+ **MİP** tarafından bir planlı sipariş yaratıldığında, sipariş miktarına bağlı olarak doğru üretim versiyonu seçilir ve daha sonra doğru üretim yöntemi çizelgelenir.

+ Sistemde malzemeyi farklı üretme yollarından her biri **versiyon** olarak geçer.

+ Üretim versiyonları malzeme ana verisi ile MİP 4 görünümünde, iş planlaması görünümünde veya **C223** işlem kodu ile oluşturulabilmektedir.
  + Üretim versiyonu butonu basıldığında yeni açılan pencerede üretim versiyonu numarası, tanımı, geçerlilik başlangıç tarihi ve geçerlilik bitiş tarihi girilir.
  + **Ayrıntılar butonu** ile üretim versiyonuna ilişkin iş planı ve ürün ağacı tayini gerçekleştirilir.
  + **Kontrol et butonu** ile seçilen ürün ağacı ve iş planının geçerli olup olmadığı değerlendirilir ve üretim versiyonun tutarlılığı denetlenir. 

## 🏤 Değişiklik Numarası

+ Değişiklik Numarası;
  + Yapılan değişikliklerin ne zaman geçerli olacağını,
  + Hangi nesneleri etkilediğini,
  + Kim tarafından yapıldığını,
  + Hangi revizyon kapsamında olduğunu kontrol eden bir mekanizmadır.
 
📌  Özellikle canlı (PRD) sistemlerde, ana veriye doğrudan müdahale etmek yerine Change Number üzerinden değişiklik yapılması önerilir / zorunlu tutulur.

+ **CC01** işlem kodu ile değişiklik numarası oluşturulabilir.

+ Burada;
  + Geçerlilik başlangıç tarihi
  + Gerekirse referans nesne
  + Açıklama
  + Değişiklik türü tanımlanır.
 
+ **CC05** işlem kodu ile belirli bir nesne için hangi değişiklik numaralarının kullanıldığını görebiliriz.

+ **CC07** işlem kodu ile belirli bir değişiklik numarasının hangi nesneleri etkilediğini görebiliriz.

📌 Canlı sistemlerde yapılan tüm değişiklikler **değişiklik numarası** ile yapılır.  










