# SAP PP Uygulama Senaryosu 

**STECH Elektrikli Scooter Üretim Süreci**

---

# 1. Senaryo 

Bu uygulamada PP modülü kullanılarak bir mamulün üretim süreci uçtan uca gösterilmiştir. 

Üretilecek ürün:
**ST-SCOOTER-1000 (STECH Elektrikli Scooter)** 

Senaryo kapsamında aşağıdaki ana veriler oluşturulmuştur:

+ Hammadde Tanımları (ROH)

+ Mamul Tanımı (FERT)

+ Ürün Ağacı (BOM)

+ İş Merkezi (Work Center)

+ İş Planı (Routing)

Amaç:
SAP PP modülünde üretim sürecinin temel entegrasyon yapısını göstermek.

<br> 

# 2. Hammadde Oluşturma 

+ **İşlem Kodu:** MM01

+ **Malzeme Türü:** ROH (Hammmadde)

+ Bu adımda scooter üretiminde kullanılacak hammaddeler oluşturulmuştur.

+ Oluşturulan malzemeler:
  + ST-GOVDE-ROH
  + ST-MOTOR-ROH
  + ST-BATARYA-ROH 

## Girilen Önemli Bilgiler 

📌 **Temel Veriler 1**

+ Malzeme Tanımı: Scooter Gövdesi

+ Temel Ölçü Birimi: ADT (Adet) veya PC

+ Malzeme Grubu: 01 (veya firmanın kullandığı grup)

+ Brüt Ağırlık: 15

+ Net Ağırlık: 14

+ Ağırlık Birimi: KG

📌 **MRP1** 

+ MRP Türü: PD

+ Parti Büyüklüğü: EX

+ MRP Kontrolörü: 001

📌 **MRP2** 

+ Tedarik Türü: F (dış tedarik)

📌 **Muhasebe 1**

+ Değerleme Sınıfı: 7900

+ Fiyat Kontrolü: V (Hareketli Ortalama)

+ Hareketli Ortalama Fiyat: 1000 TRY 

❗Aynı bilgiler **ST-MOTOR-ROH ve ST-BATARYA-01** için de girilmiştir. 

❗ROH olarak tanımlanan malzemeler üretim sırasında tüketime giren hammaddelerdir. MRP çalıştırıldığında sistem bu malzemeler için satınalma isteği oluşturur.

<br> 

## 3. Mamul Oluşturma 

+ Hammaddeleri oluşturduktan sonra **FERT** oluşturuyoruz. 

+ **İşlem Kodu:** MM01 

+ **Malzeme Türü:** FERT (Mamul) 

+ Oluşturulan malzeme: ST-SCOOTER-1000

📌 **Temel Veriler 1** 

+ Malzeme Tanımı: STECH Elektrikli Scooter

+ Temel Ölçü Birimi: ADT

+ Malzeme Grubu: 02

+ Net Ağırlık: 25

+ Brüt Ağırlık: 27

+ Ağırlık Birimi: KG

📌 **MRP 1**

+ MRP Türü: PD

+ Parti Büyüklüğü: EX

+ MRP Kontrolörü: 001

📌 **MRP 2**

+ Tedarik Türü: E (Üretim)
  + FERT olduğu için üretim yapılacak.
 
📌 **MRP 3**

+ Strateji Grubu: 40 (Stok için üretim)

📌 **Muhasebe 1** 

+ Değerleme Sınıfı: 7900 

+ Fiyat Kontrolü: S

+ Standart Fiyat: 5000 TRY

❗ FERT malzemeler üretim emri ile üretilen ve stoğa giren mamullerdir.
❗ Tedarik Türü = E olması üretim sürecini tetikler.

<br> 

## 4. Ürün Ağacı Oluşturma 

+ **İşlem Kodu:** CS01
  
<img width="557" height="351" alt="cs01-01" src="https://github.com/user-attachments/assets/3be07216-42df-4ad2-8bed-5f558473e951" />

+ **Başlık Bilgileri:**
  + Malzeme: ST-SCOOTER-1000

  + Tesis: ZAKD (Impress ÜY)

  + Kullanım: 1 (Üretim)

  + Alternatif: 1

    <br> 
    
<img width="1222" height="371" alt="cs01-02" src="https://github.com/user-attachments/assets/5de6a7dd-7e29-47c4-a97b-bb399e549e9f" />

+ **Bileşen Ekranı:**
  + | Bileşen | Miktar | Ölçü Birimi |
    | :--- | :--- | :--- |
    | ST-GOVDE-ROH | 1 | ADT |
    | ST-MOTOR-ROH | 1 | ADT |
    | ST-BATARYA-ROH | 1 | ADT |

❗BOM, üretim sırasında hangi hammaddelerin hangi miktarda tüketileceğini belirler.

<br> 

## 5. İş Merkezi Oluşturma 

+ **İşlem Kodu:** CR01 

<img width="451" height="358" alt="cr01-01" src="https://github.com/user-attachments/assets/3c6819de-b7ce-4ffa-bab6-ce70f648970c" />

<br> 

+ **İlk Ekran:**
  + İş Merkezi: SCOT_MON
  + Tesis: ZAKD
  + İş Merkezi Türü: 0001 (Makine)
 
+ ***Temel Veriler:**
  + Tanım: Scooter Montaj Hattı
  + Sorumlu Kişi: 001
 
+ **Kapasite:**
  + Kapasite Türü: 001 (Makine) 
  + Kapasite Kategorisi: 001
  + Kapasite Sayısı: 1    

❗İş merkezi, üretim operasyonlarının gerçekleştirildiği fiziksel veya mantıksal üretim birimidir. Aynı zamanda maliyetlerin toplandığı yerdir.

## 6. İş Planı Oluşturma 

+ **İşlem Kodu:** CA01
  <br> 
<img width="612" height="384" alt="ca01-01" src="https://github.com/user-attachments/assets/c54a5bf0-b784-4b77-94fe-6b8f276253a7" />
  <br>
  
+ **Başlık Bilgileri:**
  + Malzeme: ST-SCOOTER-1000
  + Tesis: ZAKD
  + Kullanım: 1
  + Durum: 4 (Onaylandı)  
  
  <br> 
<img width="804" height="651" alt="ca01-02" src="https://github.com/user-attachments/assets/7a4f6567-d3af-4082-aa1b-7da54df5d183" />
  <br> 


❗İş planı, üretim sırasında hangi operasyonların hangi iş merkezinde ve ne kadar sürede yapılacağını belirler.
  

### Hata Senaryosu 

+ Malzemeler eğer ROH yerine FERT açılsaydı ne olurdu ?

++ Malzeme türü değiştiğinde sadece muhasebe hesabı değil, tedarik tipi, MRP davranışı ve maliyet nesnesi de değişir. ROH yerine FERT tanımlanırsa sistem malzemeyi satın alınacak değil üretilecek olarak algılar. Bu da gereksiz üretim emirlerine, yanlış kapasite planlamasına ve hatalı maliyet akışına sebep olur.


