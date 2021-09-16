# 1. Ön Hazırlık Aşaması
Bu evrede, eklentinin limana ve sunucuya eklenmesi gösterilmektedir. Ayrıca tüm işlemlerin götürülmesi için bazı gereklilikler de listelenmiştir.
<br>

## 1.1. Gereklilikler
- Eklentinin kullanılabilmesi için **Samba**'nın sunucuda yüklü olması gerekmektedir.
- Samba Sunucusunun Domain Sunucusu ile aynı Domain içerisinde olması gerekmektedir.
<br>

## 1.2. Sambafileshare Eklentisinin Limana Eklenmesi
Fileshare eklentisinin Limana eklemek için **Eklenti Mağazasına** gidilir.  
![2021-09-14_15-25](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-14_15-25.png)
<br>

Eklenti Mağazası içerisinde **Eklenti yükle** butonu ile Fileshare eklentisi seçilir ve Limana ekleme işlemi gerçekleştirilir.

![2021-09-14_15-26](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-14_15-26.png)
<br><br>

![2021-09-14_15-27](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-14_15-27.png)
<br>

Yükle butonuna basılır ve karşılaşılan Onay penceresinde **Tamam** seçeneği seçilerek onay verilir. Böylelikle eklenti başarı ile yüklenmiş olur. 
<br>

Eğer halihazırda fileshare eklentisinin en güncel sürümü limanda yüklü ise "*Eklentinin bu sürümü zaten yüklü*" uyarısı ile karşılaşılır.  
<br>

## 1.3. Sambafileshare Eklentisinin Sunucuya Eklenmesi

Fileshare eklentisini kullanabilmek için Liman üzerinde eklenmiş bir Samba sunucu bulunması gerekmektedir. Samba sunucusuna tıklanılır ve sunucu detayları seçeneği seçilir.
<br> 

![2021-09-14_15-28](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-14_15-28.png)
<br>

Açılan pencerede **Eklentiler** sekmesine gidilir.
<br>

![2021-09-14_15-40](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-14_15-40.png)
<br>

Daha sonra yeşil "+" butonuna basılır.<br>

![2021-09-14_15-41](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-14_15-41.png)
<br>

Açılan pencerede Sambafileshare eklentisi seçilir ve ekle butonuna basılır.<br>

![2021-09-14_15-42](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-14_15-42.png)
<br>

Eklenti, başarılı bir şekilde yüklendiğinde hem *Eklentiler* sekmesi altında görüntülenecektir hem de sol taraftaki *Sunucu Bilgileri* kısmında eklentinin adı yazacaktır.<br>

![2021-09-14_15-45](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-14_15-45.png)
<br>

Sol tarafta bulunan sunucular listesinden sunucu seçilir ve **Sambafileshare** seçeneği seçilir böylelikle sunucu üzerinde fileshare eklentisi arayüzüne geçiş yapılır. <br>

![2021-09-14_15-49](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-14_15-49.png)
<br>

Açılacak arayüzde kullanıcıdan 3 farklı alan istenmektedir. Bunlar: <br>
- Kullanılacak Domain sunucusu: Domain eklentisinin kurulu olduğu, içerisinde kullanıcıları ve bilgisayarları barındıran sunucu.
- Ağaç için dosya yolu: Paylaşımların tutulacağı dizin
- Paylaşım Dosya Yolu: Kullanıcıların kendi paylaşım klasörlerinin oluşturulduğu dizin. (Sunucu üzerinde farklı bir klasör seçilebilir. MSB tarafında bu kısmı ilgilendiren **Kullanıcı Dizinleri** sekmesi bulunmadığı için şimdilik herhangi bir işlevi yoktur.)

![2021-09-15_08-33](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_08-33.png)
<br>

Boşluklar gerekli seçenekler ile doldurulur. Paylaşım dosya yolu, ağaç dosya yolu ile aynı dizin için belirtilebilir. Fakat kullanıcı paylaşımlarının daha düzenli durması için farklı bir dizinde bir klasör oluşturulup o klasör paylaşım yolu olarak belirtilebilir.
![2021-09-15_08-34](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_08-34.png)
<br>


Yukarıdaki görselde domain sunucusu olarak "SambaSunucu01" sunucusu, ağaç için dosya yolu olarak "/srv" dizini ve paylaşım dosya yolu olarak yeni oluşturulmuş "usershares" adlı dizin seçilmiştir. 

Gerekli seçimler yapıldıktan sonra **KAYDET** butonu ile ayarlar kaydedilir.

Arayüzde aşağıdaki uyarı ile karşılaşılır. Söylendiği gibi **Acl paketini depodan kur** seçeneği ile gerekli kurulum gerçekleştirilir.

![2021-09-15_08-47](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_08-35.png)

Gerekli kurulum gerçekleştiğinde paylaşım eklentisinin arayüzü ekranda belirecektir.

![2021-09-15_08-53](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_08-53.png)

# 2. Sambafileshare Eklentisi Versiyon 0.45 Kullanım Kılavuzu
Bu başlık altında eklenti ve özelliklerinin nasıl kullanıldığı anlatılmıştır.<br>

## 2.1. Paylaşım İçin Klasör Oluşturulması
Paylaşım oluşturulabilmesi için bir klasör oluşturulması gerekmektedir. <br>
Bu işlem için Ağaç dosya yolu olarak belirtilen dizine sağ tıklanılır ve **Yeni Klasör** seçeneği seçilir.<br>

![2021-09-15_09-37](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_09-37.png)
<br>

Klasöre bir isim verildikten sonra **Oluştur** butonuna tıklanılır.<br>

![2021-09-15_09-39](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_09-39.png)
<br>

Böylelikle klasör başarılı bir şekilde oluşturulur.<br>

![2021-09-15_09-43](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_09-43.png)
<br>

### 2.1.1. İç İçe (Nested) Klasör Oluşturma
Klasör oluşturma ana dizin üzerinden gerçekleştirilebildiği gibi, alt klasörler içerisinde de gerçekleştirilebilir.<br>

![2021-09-15_09-45](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_09-45.png)
<br>


## 2.2. Paylaşım Oluşturma

Paylaşım oluşturma işlemi 2 farklı yöntemle gerçekleştirilebilir.

### 2.2.1. Yeni Paylaşım Butonu İle Paylaşım Oluşturma

Arayüzde gözüken **+ Yeni Paylaşım** butonu kullanılarak paylaşım oluşturulabilir. 

![2021-09-15_09-55](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_09-55.png)

Butona basıldığında paylaşım oluşturma ekranı açılmaktadır. Bu ekranda **Ayarlar** ve **Erişim Yetkileri** adlı 2 farklı sekme bulunmaktadır. 

#### 2.2.1.1. Ayarlar Sekmesi

Bu sekme üzerinde bulunan seçenekler aşağıdaki gibidir:

- Paylaşım adı: Oluşturulacak paylaşıma verilecek isim.
- Paylaşım yolu: Oluşturulacak paylaşımın adres gösterdiği dizin.
- Açıklama: Paylaşım hakkında belirtilecek notlar. (boş bırakılabilir)
- Keşfedilebilir: Bu seçenek seçildiğinde paylaşım kullanıcılar için gözle görülür hale gelir.
- Misafir Erişebilir: Guest olarak belirlenen kullanıcıların erişim sağlayabilmesine olanak tanır.
- Dosya boyutunu belirle: Paylaşımın alacağı max boyutu belirlemeye olanak tanır.



![2021-09-15_10-28](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_10-28.png)



#### 2.2.1.2. Erişim Yetkileri Sekmesi

Bu sekme üzerinde bulunan seçenekler aşağıdaki gibidir:

- Paylaşılacak Kullanıcılar: Bu paylaşıma erişebilecek kullanıcıların seçilmesi
- Paylaşılmayacak Kullanıcılar: Bu paylaşıma erişimi yasaklanmış kullanıcıların seçilmesi



![2021-09-15_10-30](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_10-30.png)



Bu seçenekler istenildiği gibi doldurulduğunda **Kaydet** butonu ile paylaşım oluşturulur.



### 2.2.2. Klasör Üzerinden Paylaşım Oluşturma

Halihazırda bulunan bir klasör için paylaşım oluşturulabilir. Paylaşım oluşturmak için istenilen klasöre sağ tıklanarak **Paylaşım Oluştur** seçeneği seçilir.

![2021-09-15_09-51](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_09-51.png)



Paylaşım oluşturma ekranında **Ayarlar** ve **Erişim Yetkileri** adlı 2 farklı sekme bulunmaktadır.

#### 2.2.2.1. Ayarlar Sekmesi

Bu sekme üzerinde bulunan seçenekler aşağıdaki gibidir:

- Paylaşım adı: Oluşturulacak paylaşıma verilecek isim.
- Paylaşım yolu: Dokunulmaz hale gelir. Bu kısım sağ tıklanılan klasör ile otomatik olarak doldurulur.
- Açıklama: Paylaşım hakkında belirtilecek notlar. (boş bırakılabilir)
- Keşfedilebilir: Bu seçenek seçildiğinde paylaşım kullanıcılar için gözle görülür hale gelir.
- Misafir Erişebilir: Guest olarak belirlenen kullanıcıların erişim sağlayabilmesine olanak tanır.
- Dosya boyutunu belirle: Paylaşımın alacağı max boyutu belirlemeye olanak tanır.



![2021-09-15_10-35](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_10-35.png)



#### 2.2.2.2. Erişim Yetkileri Sekmesi

Bu sekme üzerinde bulunan seçenekler aşağıdaki gibidir:

- Paylaşılacak Kullanıcılar: Bu paylaşıma erişebilecek kullanıcıların seçilmesi
- Paylaşılmayacak Kullanıcılar: Bu paylaşıma erişimi yasaklanmış kullanıcıların seçilmesi



![2021-09-15_10-36](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_10-36.png)



Bu seçenekler istenildiği gibi doldurulduğunda **Kaydet** butonu ile paylaşım oluşturulur.



## 2.3. Paylaşımı Düzenleme

Oluşturulan paylaşımın ayarları daha sonradan değiştirilebilir. Bunun için düzenlenmesi istenilen paylaşıma sağ tıklanılır ve **Düzenle** seçeneği seçilir.

![2021-09-15_11-15](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_11-15.png)



Açılan pencerede paylaşım oluşturulurken karşılaşılan 2 sekme görüntülenir. 

Ayarlar sekmesinde düzenlenebilecek seçenekler:

* Açıklama: Paylaşımın açıklaması değiştirilebilir.
* Keşfedilebilir seçeneği: Kullanıcıların paylaşımı görme özelliği eklenebilir ya da kaldırılabilir.
* Misafir Erişebilir seçeneği: Misafir kullanıcıların paylaşıma erişimleri değiştirilebilir.

![2021-09-15_11-18](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_11-18.png)



Bu sekme üzerinde **Paylaşım adı** ve **Paylaşım Yolu** değiştirilememektedir.

Erişim Yetkileri sekmesinde düzenlenebilecek seçenekler:

* Paylaşılacak Kullanıcılar: Paylaşıma erişebilecek kullanıcılar eklenip çıkarılabilir.
* Paylaşılmayacak Kullanıcılar: Paylaşıma erişmesi yasak olan kullanıcılar eklenip çıkarılabilir.

![2021-09-15_11-19](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_11-19.png)



## 2.4 Paylaşım İzinleri

 Paylaşımın kullanıcı, grup ve diğer kullanıcılar için erişim izinleri değiştirilebilir. Bunun için paylaşıma sağ tıklanılır ve **Paylaşım İzinleri** seçeneği seçilir.

![2021-09-15_11-24](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_11-24.png)



Açılan pencerede paylaşım hakkında aşağıdakiler yer alır:

- Dosya yolu: Paylaşımın oluşturulduğu dizin 
- Kullanıcı: Paylaşımın sahibi olan kullanıcı ve yetkileri
- Grup: Paylaşımın sahibi olan grup ve yetkileri,
- Diğer: Diğer kullanıcıların yetkisi,
- Kullanıcıya İzin Ekle butonu: Paylaşıma erişim izni ve yetkileri verilecek kullanıcı eklemek için kullanılır.
- Gruba İzin Ekle butonu: Paylaşıma erişim izni ve yetkileri verilecek grup eklemek için kullanılır.
- Paylaşım İzinlerini Değiştir butonu: Kullanıcı, Grup ve Diğer için erişim yetkilerinin değiştirilmesi için kullanılır.
- Alt kısımdaki tablo: Paylaşım için yetki verilen kullanıcı ve gruplar yer alır.

![2021-09-15_11-29](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_11-29.png)



### 2.4.1 Paylaşım İzinlerinin Değiştirilmesi

Paylaşım üzerindeki kullanıcı, grup ve diğer kullanıcıların yetkilerinin düzenlenmesi işlemidir. Bu işlem **Paylaşım İzinlerini Değiştir** butonu ile açılan pencerede gerçekleştirilir.

![2021-09-15_11-39](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_11-39.png)



Butona basıldıktan sonra gelen pencere şu şekildedir:

![2021-09-15_11-40](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_11-40.png)



Bu pencerede:

- User = Kullanıcı (dosya sahibi) için Okuma-Yazma yetkilerini düzenler
- Group = Grup için Okuma-Yazma yetkilerini düzenler
- Other = Diğer kullanıcılar için Okuma-Yazma yetkilerini düzenler 
- Özyineli = Verilen veya alınan izinlerin, paylaşımın bulunduğu dizinin alt dizinleri içinde geçerli olmasını sağlar.



**Örnek: Paylaşımın Grup ve Diğer Kullanıcılar için Tüm Yetkilerinin Kaldırılması**

Paylaşımın genel görünümü:

![2021-09-15_11-46](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_11-46.png)

İzinler penceresi:

![2021-09-15_11-47](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_11-47.png)

İzinler penceresinden izinlerin değiştirilmesi:

![2021-09-15_11-48](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_11-48.png)

Paylaşımın, izinler değiştirildikten sonraki genel görünümü:

![2021-09-15_11-49](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_11-49.png)



### 2.4.2 Kullanıcıya İzin Ekleme

Paylaşıma kullanıcı atama ve yetkilendirme işlemidir. Bu işlem **Kullanıcıya İzin Ekle** butonu sayesinde gerçekleştirilir.

![2021-09-15_11-55](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_11-55.png)

Butona basıldıktan sonra gelen pencere şu şekildedir:

![2021-09-15_12-41](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_12-41.png)



Bu pencerede:

- Kullanıcı kısmında yetki verilecek kullanıcı seçilir.
- Okuma seçeneği, seçilen kullanıcıya okuma (Read) yetkisi verir.
- Yazma seçeneği, seçilen kullanıcıya yazma (Write) yetkisi verir.
- Özyineli seçeneği, verilen yetkilerin paylaşımın alt dizinlerinde de geçerli olmasını sağlar.



Bir kullanıcı seçip istenilen yetkiler verildiğinde **Paylaşım İzinleri** penceresinin alt kısmındaki tabloda seçilmiş olan kullanıcı ve o kullanıcıya atanmış izinler görüntülenecektir.

![2021-09-15_12-48](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_12-48.png)



### 2.4.3. Kullanıcı İznini Düzenleme

Bu işlem paylaşım üzerindeki kullanıcı izinlerini düzenleme işlemidir. Bunun için **Paylaşım İzinleri** penceresinin alt kısmındaki tabloda istenilen kullanıcıya sağ tıklanılır ve **Düzenle** seçeneği seçilir.   

![2021-09-16_08-00](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_12-49.png)



Daha sonra kullanıcıya istenilen izinler verilir veya çıkartılır. İzinler, özyineli olarak da verilebilir.

![2021-09-15_12-49-1](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_12-49-1.png)



Düzenle butonu ile izinler kayıt edildiğinde, tabloda kullanıcının izinlerinin değişmiş olduğu gözükmektedir.

![2021-09-15_12-49-2](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_12-49-2.png)



### 2.4.4. Kullanıcı İznini Silme

Paylaşımda yetkileri olan kullanıcının yetkilerinin silinmesi işlemidir. Bu işlem **Paylaşım İzinleri** penceresinin alt kısmındaki tabloda kullanıcıya sağ tıklayıp **Sil** ve **Özyineli Sil** işlemleri ile gerçekleştirilir.

- Sil: Kullanıcının geçerli dizin üzerindeki yetkilerinin kaldırılması işlemidir.
- Özyineli Sil: Kullanıcının geçerli dizin ve tüm alt dizinlerindeki yetkilerinin kaldırılması işlemidir.

![2021-09-15_12-49-3](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_12-49-3.png)



### 2.4.5. Gruba İzin Ekleme

Paylaşım için grup atama ve yetkilendirme işlemidir. Bu işlem **Gruba İzin Ekle** butonu sayesinde gerçekleştirilir.

![2021-09-15_12-50](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_12-50.png)



Butona basıldıktan sonra karşılaşılan pencere aşağıdaki gibidir:

![2021-09-15_12-50_1](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_12-50_1.png)



Bu pencerede:

- Grup kısmında yetki verilecek grup seçilir.
- Okuma seçeneği, seçilen gruba okuma (Read) yetkisi verir.
- Yazma seçeneği, seçilen gruba yazma (Write) yetkisi verir.
- Özyineli seçeneği, verilen yetkilerin paylaşımın alt dizinlerinde de geçerli olmasını sağlar.



Bir grup seçip istenilen yetkiler verildiğinde **Paylaşım İzinleri** penceresinin alt kısmındaki tabloda seçilmiş olan grup ve o gruba atanmış izinler görüntülenecektir.

![2021-09-15_13-04](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_13-04.png)



### 2.4.6.  Grup İznini Düzenleme

Bu işlem paylaşım üzerindeki grubun izinlerini düzenleme işlemidir. Bunun için **Paylaşım İzinleri** penceresinin alt kısmındaki tabloda istenilen gruba sağ tıklanılır ve **Düzenle** seçeneği seçilir.   

![2021-09-16_08-22](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-16_08-22.png)



Daha sonra gruba istenilen izinler verilir veya çıkartılır. İzinler, özyineli olarak da verilebilir.

![2021-09-16_08-26](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-16_08-26.png)



Düzenle butonu ile izinler kayıt edildiğinde, tabloda grubun izinlerinin değişmiş olduğu gözükmektedir.

![2021-09-16_08-26_1](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-16_08-26_1.png)



### 2.4.7. Grup İznini Silme

Paylaşımda yetkileri olan grubun yetkilerinin silinmesi işlemidir. Bu işlem **Paylaşım İzinleri** penceresinin alt kısmındaki tabloda gruba sağ tıklayıp **Sil** ve **Özyineli Sil** işlemleri ile gerçekleştirilir.

- Sil: Grubun geçerli dizin üzerindeki yetkilerinin kaldırılması işlemidir.
- Özyineli Sil: Grubun geçerli dizin ve tüm alt dizinlerindeki yetkilerinin kaldırılması işlemidir.

![2021-09-16_08-32](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-16_08-32.png)



## 2.5. Paylaşımın Boyutunun Ayarlanması

İstenilen paylaşım klasörünün ve alt klasörlerin boyutuna belirli bir kotanın koyulması işlemidir. Bu işlem eklenti arayüzünde paylaşıma sağ tıklayıp **Boyut Ayarla** seçeneği seçilerek gerçekleştirilir. 

![2021-09-16_08-46](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-16_08-46.png)



Açılan pencerede paylaşımın referans gösterdiği dosyanın boyutu belirlenir ve **Ayarla** butonu ile kaydedilir.

![2021-09-16_08-48](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-16_08-48.png)



Böylelikle paylaşımın adreslediği klasör bir kota kazanmış olur. Kullanıcılar ve gruplar bu klasör (ve alt klasörler) içerisinde dosya yükleme-oluşturma işlemlerinde belirlenmiş boyutu geçemez hale gelir.



## 2.6. Paylaşımın Silinmesi

Kullanılmayan veya istenmeyen paylaşımın kaldırılması işlemidir. Bu işlem eklentinin arayüzünde seçilen paylaşıma sağ tıklayıp **Paylaşımı Sil** seçeneği ile gerçekleştirilir. 

![2021-09-16_08-54](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-16_08-54.png)



Bu seçenek seçildiğinde onay penceresi gelir. Onay verildiğinde ise paylaşım silinmiş olur.

![2021-09-16_09-16](https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-16_09-16.png)





