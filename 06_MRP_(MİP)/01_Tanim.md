# Malzeme İhtiyaç Planlaması 

+ Malzeme İhtiyaç Planlaması (MİP) hangi malzemelerin hangi miktarlarda ve hangi tarihlerde üretilmesi ya da tedarik edilmesi gerektiğini ortaya koyan, malzemenin ihtiyaç duyulan zamanlarda elde bulunurluğunu sağlayan programdır.

+ **Ürün ağacı verisini**, **envanter verisini** ve **ana üretim çizelgeleme** verilerini kullanarak malzeme ihtiyaçlarını hesaplar.

+ MİP ile ürün ağacı bazında en üst seviyedeki üründen başlayarak en alt seviyeye kadar net ihtiyaç karşılanır.

+ **Net ihtiyaçlar**, üretim ve satın alma için program tarafından **otomatik** olarak oluşturulan tedarik önerileri ile karşılanmaktadır.

+ MİP ile çalışmak için malzeme ana verileri, ürün ağacı, işyeri, iş planı bileşenlerinin sistem üzerinde tanımlı olması gerekir.

+ **Planlı Sipariş:** Malzeme ihtiyaç planlamasına dahil olan her bir malzeme için, ihtiyaç miktarı tedarik miktarından fazla ise bu ihtiyaç miktarını tedarik miktarına eşitleyecek şekilde üretilen malzemelerde üretim önerisi yaratma.

+ **Satınalma Talebi:** Dışarıdan tedarik edilen malzemelerde açılan öneri.

+ Stok, planlı sipariş, üretim siparişi, satın alma talebi satın alma siparişi ve stok nakli siparişleri ise **tedarik miktarlarını** oluşturur.

+ Ürün ağaçları aracılığıyla bir üst seviyede yaratılan planlı siparişler alt seviye için bir ihtiyaç ortaya çıkartır, bu ihtiyaçlar **ikincil ihtiyaçlar** olarak tanımlanmaktadır.

+ Ürün ağaçlarındaki en alt malzemeye ulaşılana kadar negatif değerleri pozitif değerlerle dengelemek için **planlı sipariş** ya da **satın alma talebi** oluşturmaya devam edilir.

📌 SAP sisteminde **tüketime dayalı planlama** ve **plana dayalı malzeme ihtiyaç planlaması** en temel iki yöntem olarak kullanılmaktadır. 

+ Tüketim bazlı olanlama geçmiş tüketim verilerinden yararlanarak yeni bir ihtiyaç belirlemeyi hedef alır.
  + Bu planlama yöntemine en basit örnek **yeniden sipariş seviyesine göre planlama**dır.
  + Yeniden sipariş seviyesi planlaması, stok seviyesi tanımlanmış bir miktar altına düştüğünde sistemin yeniden tedarik önerisi oluşturmasını tetikler.
 
+ Plana dayalı MİP, planlı birincil ihtiyaçlara ya da müşteri siparişlerine dayanmaktadır.
  + Bağımsız ihtiyaçlar ve gerçek satış ihtiyaçlarından yola çıkarak alt seviyeler için türetilmiş olan bağımlı taleplerin planlanmasını esas alan bir analitik prosedürdür.
 
❗Tüketime dayalı planlama geçmiş verilere dayalı olduğundan geçmişe yönelik bir planlama şekli, plana dayalı ise aslında varolan ihtiyaç miktarlarına dayalı olduğundan planlama gelecek odaklı olduğu söylenebilir. 

+ Malzeme ihtiyaç planlaması aşağıdaki adımlardan oluşur:

  + **1)** Planlamaya dahil olacak malzemelerin belirlenmesi için planlama dosyası girişleri kontrol edilir.
 
  + **2) Net İhtiyaç Hesaplaması:** Açık olan tüm ihtiyaçlar (satış siparişleri, birincil ve ikincil ihtiyaçlar vb.), girişler (satınalma talepleri, satınalma siparişleri vb.) ve mevcut stok göz önünde bulundurularak her bir malzeme için net ihtiyacın ne kadar olduğu hesaplanır.
 
  + **3) Parti Büyüklüğü Hesaplama:** Hesaplanan net ihtiyaca karşılık ne kadarlık tedarik yapılacağı hesaplanır.
 
  + **4) Terminleme:** İhtiyacın bulunduğu tarihte malzemenin hazır edilmesi için ne kadar önceden sipariş edilmesi gerektiği hesaplanır.
 
  + **5) Tedarik Türünün Belirlenmesi:** İhtiyaca karşılık hesaplanan parti büyüklüğü kadar tedarik türüne göre **planlı sipariş** veya **satınalma talebi** oluşturulmaktadır.
 
  + **6) Ürün Ağacı Açılımı:** Net ihtiyaca karşılık oluşturulan planlı siparişler için ürün ağacı açılımı yapılarak bileşen malzemelere ihtiyaç aktarımı (ikincil ihtiyaçlar) yapıılır.
 
--- 

## Parti Büyüklüğü 

| MİP Parti Büyüklüğü | Prosedür | Gösterge |
| :--- | :--- | :--- |
| EX | İhtiyaca göre parti büyüklüğü hesaplaması | E – İhtiyaca göre parti büyüklüğü |
| FX | Sabit parti büyüklüğü | F – Sabit parti büyüklüğü |
| FS | Sabit parti büyüklüğü (bölmeli) | F – Sabit parti büyüklüğü (bölünmüş sipariş) |
| HB | Maksimum stok seviyesine tamamlama | H – Stok seviyesine tamamlama |
| MB | Aylık parti büyüklüğü | P – Dönemsel (Aylık) |
| TB | Günlük parti büyüklüğü | P – Dönemsel (Günlük) |
| WB | Haftalık parti büyüklüğü | P – Dönemsel (Haftalık) |
| WI | Takvim haftasına göre parti büyüklüğü | P – Dönemsel (Takvim haftası) |
| DY | Dinamik parti büyüklüğü | D – Dinamik hesaplama |
| PK | Planlama takvimine göre parti büyüklüğü | P – Planlama takvimi |
| SP | Planlama stratejisine bağlı parti büyüklüğü | S – Strateji bazlı |


<br> 

## Bağımsız İhtiyaç (Tahmin) - MD61 (PP) 

Üretim planlamasında müşteri siparişinden bağımsız olarak oluşturulan tahmini ihtiyaçlara **Planlı Bağımsız İhtiyaç (PIR)** denir.

<img width="701" height="470" alt="md61" src="https://github.com/user-attachments/assets/9626c0ca-8781-4aed-933b-392d7cd05f3b" />

<br> 

+ İşlem Kodu: MD61

+ Amaç: Gelecekte oluşması beklenen talebi sisteme girmek

+ Kullanım Senaryosu: Make-to-Stock (MTS) üretim yapan firmalar

Bu işlem sonucunda sistem, ilgili malzeme için planlama sırasında dikkate alınacak talep oluşturur.

<br> 

## Müşteri Siparişi - VA01 (SD) 

Gerçek müşteri talebi, satış siparişi ile sisteme girilir.

<img width="618" height="359" alt="va01" src="https://github.com/user-attachments/assets/a0a025ee-dbac-4ca5-992a-1e7dc8236f51" />

<br>

+ İşlem Kodu: VA01

+ Modül: SD

+ Amaç: Müşteriden gelen gerçek talebi kaydetmek

Eğer planlama stratejisi müşteri siparişine bağlı çalışıyorsa (örneğin MTO), bu sipariş MRP tarafından doğrudan dikkate alınır.

❗MRP bazı firmalarda günde 1 kez, bazı firmalarda günde 2 kez çalıştırılır.

❗İş yoğunluğuna göre gece batch job olarak planlanabilir.

<br>

## MRP Çalıştırma İşlemleri 

### MD01 - Toplu MRP (Plant Bazlı) 

<img width="681" height="578" alt="md01" src="https://github.com/user-attachments/assets/449c9223-274b-4ae9-8db1-b9ab7cc106db" />

<br>

+ Üretim yeri (Plant) bazında çalışır.

+ Seçilen üretim yerindeki tüm MRP’ye dahil malzemeleri planlar.

### MD02 – Tek Malzeme Bazlı MRP

<img width="733" height="622" alt="md02" src="https://github.com/user-attachments/assets/638afa4b-3792-4155-8df6-a75e9a55419a" />

<br>

+ Belirli bir malzeme için çalışır.

+ Test ve eğitim ortamlarında en sık kullanılan işlem kodudur.

📌 MİP Alanı sayesinde:
  + Belirli depo yerleri
  + Belirli üretim alanları
  + MİP'e dahil edilir veya hariç tutulabilir.
  + Böylece planlama, tüm plant yerine belirli bir alan için yapılabilir.

📌 **İşleme Anahtarı (Processing Key)**
  + NETCH = Net Change Planning in Total Horizon
    + Son MRP çalışmasından sonra değişiklik olan malzemeleri planlar.
    + Tüm malzemeleri yeniden planlamaz.

### MD01N – MRP Live 

<img width="718" height="525" alt="md01n" src="https://github.com/user-attachments/assets/59faeec6-ea33-4819-8a4c-d4f5e70be562" />

<br>

+ SAP S/4HANA ile gelen yeni nesil MRP programıdır.

+ Daha hızlı çalışır (HANA optimizasyonu).

+ Büyük veri hacmi olan firmalarda tercih edilir.






