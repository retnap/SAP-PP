# Strateji Grupları 

## 📌 10 - Make to Stock (Tüketime Dayalı Üretim) 

Strateji 10 = Sadece Tahmine dayalı üretim 

### Süreç Akışı 

**1.** MD61 → Planlanan Bağımsız İhtiyaç (PIR) girilir

**2.** MD02 → MRP çalıştırılır

**3.** Sistem planlı sipariş oluşturur

**4.** Üretim yapılır, stok oluşur

**5.** VA01 ile müşteri siparişi girildiğinde stoktan düşer

### Kontrol Ekranı 

📌 **MD04** - Stock/Requirements List, İhtiyaçları ve stokları anlık görüntüleme 

<img width="771" height="405" alt="md04" src="https://github.com/user-attachments/assets/e5c3e420-9d3d-4326-b98a-57eb4ddea68d" />

<br>

+ MD04 ekranında:
  + PIR (MD61 ile girilen tahmin)
  + Planlı sipariş
  + Stok miktarı
  + Müşteri siparişi aynı ekranda görülebilir.
 
<br> 

## 📌 20 - Make to Order (Müşteri Siparişine Dayalı Üretim) 

Strateji 20 = Sipariş Gelmeden Üretim Yok

### Süreç Akışı 

**1**. VA01 → Satış siparişi oluşturulur

**2.** MRP çalıştırılır

**3.** Sistem siparişe özel planlı sipariş oluşturur

**4.** Üretim tamamlanır

**5.** Ürün doğrudan ilgili siparişe gider

<br> 

## 📌 Planning with Final Assembly (Hem Tahmin Hem Sipariş)

Strateji 40 = Tahmin + Müşteri Siparişi birlikte çalışır.

### Süreç Akışı 

**1.** Önce tahmin girilir (**MD61**). 

**2.** MRP üretimi planlar. 

**3.** Müşteri siparişi geldiğinde tahmin düşülür.

❗Buradaki önemli kavram **mahsuplaştırma**dır. 

### Mahsuplaştırma 

+ Strateji 40’ta müşteri siparişi geldiğinde:
  + Sistem tahmini tüketir (mahsuplaştırır).
 
+ Örnek olarak:
  + 100 adet tahmin vardı.
  + 30 adet siparişten geldi.
  + Kalan tahmin 70 olur.
 
❕Bu kontrol **MD63** ekranından görüntülenebilir. 

<img width="655" height="557" alt="md63" src="https://github.com/user-attachments/assets/6d9bdea8-8aa6-4476-b1d2-d88ab45db6fd" />

<br>

+ MD63 ihtiyaç ekranında:
  + Toplam tahmin
  + Tüketilen miktar
  + Kalan miktar net şekilde takip edilir.
 
### Mahsuplaştırma Türleri 

Strateji 40'ta mahsuplaştırma üç şekilde olabilir:

**1. Geriye Dönük (Backward Consumption)**

Sipariş, geçmişteki tahmini tüketir. 

**2. İleriye Dönük (Forward Consumption)**

Sipariş, ilerideki tahmini tüketir. 

**3. Her iki yönlü (Backward + Forward)**

Belirlenen süre aralığında en uygun tahmini tüketir.

<br> 

## MD04 ile Analiz 

Strateji 40 ve MD04 ekranında aşağıdakileri birlikte görürüz:

+ PIR (VSF)
+ Sales Order (CUS)
+ Planlı Sipariş (PlOrd)
+ Stok

Sipariş geldiğinde:
  + PIR miktarı azalır.
  + Yeni planlı sipariş ihtiyacı değişir.

❗Bu ekran canlı analiz için en kritik ekrandır.


