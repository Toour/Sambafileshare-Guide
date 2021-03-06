# 1. Ön Hazırlık Aşaması
Bu evrede, eklentinin limana ve sunucuya eklenmesi gösterilmektedir. Ayrıca tüm işlemlerin götürülmesi için bazı gereklilikler de listelenmiştir.
<br>

## 1.1. Gereklilikler
- Eklentinin kullanılabilmesi için **Samba**'nın sunucuda yüklü olması gerekmektedir.
- Samba Sunucusunun Domain Sunucusu ile aynı Domain içerisinde olması gerekmektedir.
<br>

## 1.2. Sambafileshare Eklentisinin Limana Eklenmesi
Fileshare eklentisinin Limana eklemek için **Eklenti Mağazasına** gidilir. 
<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-14_15-25.png" width=300>      
</p>
  
Eklenti Mağazası içerisinde **Eklenti yükle** butonu ile Fileshare eklentisi seçilir ve Limana ekleme işlemi gerçekleştirilir.

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-14_15-26.png" width=600>
</p>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-14_15-27.png" width=800>      
</p>

Yükle butonuna basılır ve karşılaşılan Onay penceresinde **Tamam** seçeneği seçilerek onay verilir. Böylelikle eklenti başarı ile yüklenmiş olur. 
<br>

Eğer halihazırda fileshare eklentisinin en güncel sürümü limanda yüklü ise "*Eklentinin bu sürümü zaten yüklü*" uyarısı ile karşılaşılır.  
<br>

## 1.3. Sambafileshare Eklentisinin Sunucuya Eklenmesi

Fileshare eklentisini kullanabilmek için Liman üzerinde eklenmiş bir Samba sunucu bulunması gerekmektedir. Samba sunucusuna tıklanılır ve sunucu detayları seçeneği seçilir.
<br> 

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-14_15-28.png" width=300>      
</p>

Açılan pencerede **Eklentiler** sekmesine gidilir.
<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-14_15-40.png" width=400>      
</p>

Daha sonra yeşil "+" butonuna basılır.<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-14_15-41.png" width=400>      
</p>

Açılan pencerede Sambafileshare eklentisi seçilir ve ekle butonuna basılır.<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-14_15-42.png" width=500>      
</p>

Eklenti, başarılı bir şekilde yüklendiğinde hem *Eklentiler* sekmesi altında görüntülenecektir hem de sol taraftaki *Sunucu Bilgileri* kısmında eklentinin adı yazacaktır.<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-14_15-45.png" width=500>      
</p>

Sol tarafta bulunan sunucular listesinden sunucu seçilir ve **Sambafileshare** seçeneği seçilir böylelikle sunucu üzerinde fileshare eklentisi arayüzüne geçiş yapılır. <br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-14_15-49.png" width=300>      
</p>

Açılacak arayüzde kullanıcıdan 3 farklı alan istenmektedir. Bunlar: <br>
- Kullanılacak Domain sunucusu: Domain eklentisinin kurulu olduğu, içerisinde kullanıcıları ve bilgisayarları barındıran sunucu.
- Ağaç için dosya yolu: Paylaşımların tutulacağı dizin
- Paylaşım Dosya Yolu: Kullanıcıların kendi paylaşım klasörlerinin oluşturulduğu dizin. (Sunucu üzerinde farklı bir klasör seçilebilir. MSB tarafında bu kısmı ilgilendiren **Kullanıcı Dizinleri** sekmesi bulunmadığı için şimdilik herhangi bir işlevi yoktur.)

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_08-33.png" width=400>      
</p>

Boşluklar gerekli seçenekler ile doldurulur. Paylaşım dosya yolu, ağaç dosya yolu ile aynı dizin için belirtilebilir. Fakat kullanıcı paylaşımlarının daha düzenli durması için farklı bir dizinde bir klasör oluşturulup o klasör paylaşım yolu olarak belirtilebilir.<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_08-34.png" width=350>      
</p>


Yukarıdaki görselde domain sunucusu olarak "SambaSunucu01" sunucusu, ağaç için dosya yolu olarak "/srv" dizini ve paylaşım dosya yolu olarak yeni oluşturulmuş "usershares" adlı dizin seçilmiştir. <br>

Gerekli seçimler yapıldıktan sonra **KAYDET** butonu ile ayarlar kaydedilir. <br>

Arayüzde aşağıdaki uyarı ile karşılaşılır. Söylendiği gibi **Acl paketini depodan kur** seçeneği ile gerekli kurulum gerçekleştirilir. <br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_08-35.png" width=500>      
</p>

Gerekli kurulum gerçekleştiğinde paylaşım eklentisinin arayüzü ekranda belirecektir.<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_08-53.png" width=600>      
</p>

# 2. Sambafileshare Eklentisi Versiyon 0.45 Kullanım Kılavuzu
Bu başlık altında eklenti ve özelliklerinin nasıl kullanıldığı anlatılmıştır.<br>

## 2.1. Paylaşım İçin Klasör Oluşturulması
Paylaşım oluşturulabilmesi için bir klasör oluşturulması gerekmektedir. <br>
Bu işlem için Ağaç dosya yolu olarak belirtilen dizine sağ tıklanılır ve **Yeni Klasör** seçeneği seçilir.<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_09-37.png" width=300>      
</p>

Klasöre bir isim verildikten sonra **Oluştur** butonuna tıklanılır.<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_09-39.png" width=600>      
</p>

Böylelikle klasör başarılı bir şekilde oluşturulur.<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_09-43.png" width=300>      
</p>

### 2.1.1. İç İçe (Nested) Klasör Oluşturma
Klasör oluşturma ana dizin üzerinden gerçekleştirilebildiği gibi, alt klasörler içerisinde de gerçekleştirilebilir.<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_09-45.png" width=300>      
</p>

## 2.2. Paylaşım Oluşturma
Paylaşım oluşturma işlemi 2 farklı yöntemle gerçekleştirilebilir.<br>

### 2.2.1. Yeni Paylaşım Butonu İle Paylaşım Oluşturma

Arayüzde gözüken **+ Yeni Paylaşım** butonu kullanılarak paylaşım oluşturulabilir. <br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_09-55.png" width=300>      
</p>

Butona basıldığında paylaşım oluşturma ekranı açılmaktadır. Bu ekranda **Ayarlar** ve **Erişim Yetkileri** adlı 2 farklı sekme bulunmaktadır. <br>

#### 2.2.1.1. Ayarlar Sekmesi

Bu sekme üzerinde bulunan seçenekler aşağıdaki gibidir:<br>
- Paylaşım adı: Oluşturulacak paylaşıma verilecek isim.
- Paylaşım yolu: Oluşturulacak paylaşımın adres gösterdiği dizin.
- Açıklama: Paylaşım hakkında belirtilecek notlar. (boş bırakılabilir)
- Keşfedilebilir: Bu seçenek seçildiğinde paylaşım kullanıcılar için gözle görülür hale gelir.
- Misafir Erişebilir: Guest olarak belirlenen kullanıcıların erişim sağlayabilmesine olanak tanır.
- Dosya boyutunu belirle: Paylaşımın alacağı max boyutu belirlemeye olanak tanır.

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_10-28.png" width=700>      
</p>

#### 2.2.1.2. Erişim Yetkileri Sekmesi
Bu sekme üzerinde bulunan seçenekler aşağıdaki gibidir:<br>
- Paylaşılacak Kullanıcılar: Bu paylaşıma erişebilecek kullanıcıların seçilmesi
- Paylaşılmayacak Kullanıcılar: Bu paylaşıma erişimi yasaklanmış kullanıcıların seçilmesi

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_10-30.png" width=700>      
</p>

Bu seçenekler istenildiği gibi doldurulduğunda **Kaydet** butonu ile paylaşım oluşturulur.<br>

### 2.2.2. Klasör Üzerinden Paylaşım Oluşturma
Halihazırda bulunan bir klasör için paylaşım oluşturulabilir. Paylaşım oluşturmak için istenilen klasöre sağ tıklanarak **Paylaşım Oluştur** seçeneği seçilir.<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_09-51.png" width=300>      
</p>

Paylaşım oluşturma ekranında **Ayarlar** ve **Erişim Yetkileri** adlı 2 farklı sekme bulunmaktadır.<br>

#### 2.2.2.1. Ayarlar Sekmesi
Bu sekme üzerinde bulunan seçenekler aşağıdaki gibidir:<br>
- Paylaşım adı: Oluşturulacak paylaşıma verilecek isim.
- Paylaşım yolu: Dokunulmaz hale gelir. Bu kısım sağ tıklanılan klasör ile otomatik olarak doldurulur.
- Açıklama: Paylaşım hakkında belirtilecek notlar. (boş bırakılabilir)
- Keşfedilebilir: Bu seçenek seçildiğinde paylaşım kullanıcılar için gözle görülür hale gelir.
- Misafir Erişebilir: Guest olarak belirlenen kullanıcıların erişim sağlayabilmesine olanak tanır.
- Dosya boyutunu belirle: Paylaşımın alacağı max boyutu belirlemeye olanak tanır.

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_10-35.png" width=700>      
</p>

#### 2.2.2.2. Erişim Yetkileri Sekmesi
Bu sekme üzerinde bulunan seçenekler aşağıdaki gibidir:<br>
- Paylaşılacak Kullanıcılar: Bu paylaşıma erişebilecek kullanıcıların seçilmesi
- Paylaşılmayacak Kullanıcılar: Bu paylaşıma erişimi yasaklanmış kullanıcıların seçilmesi

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_10-36.png" width=700>      
</p>

Bu seçenekler istenildiği gibi doldurulduğunda **Kaydet** butonu ile paylaşım oluşturulur.<br>

## 2.3. Paylaşımı Düzenleme
Oluşturulan paylaşımın ayarları daha sonradan değiştirilebilir. Bunun için düzenlenmesi istenilen paylaşıma sağ tıklanılır ve **Düzenle** seçeneği seçilir.<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_11-15.png" width=300>      
</p>

Açılan pencerede paylaşım oluşturulurken karşılaşılan 2 sekme görüntülenir. <br>
Ayarlar sekmesinde düzenlenebilecek seçenekler:<br>
- Açıklama: Paylaşımın açıklaması değiştirilebilir.
- Keşfedilebilir seçeneği: Kullanıcıların paylaşımı görme özelliği eklenebilir ya da kaldırılabilir.
- Misafir Erişebilir seçeneği: Misafir kullanıcıların paylaşıma erişimleri değiştirilebilir.

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_11-18.png" width=700>      
</p>

Bu sekme üzerinde **Paylaşım adı** ve **Paylaşım Yolu** değiştirilememektedir.<br>
Erişim Yetkileri sekmesinde düzenlenebilecek seçenekler:<br>
- Paylaşılacak Kullanıcılar: Paylaşıma erişebilecek kullanıcılar eklenip çıkarılabilir.
- Paylaşılmayacak Kullanıcılar: Paylaşıma erişmesi yasak olan kullanıcılar eklenip çıkarılabilir.

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_11-19.png" width=700>      
</p>

## 2.4 Paylaşım İzinleri
Paylaşımın kullanıcı, grup ve diğer kullanıcılar için erişim izinleri değiştirilebilir. Bunun için paylaşıma sağ tıklanılır ve **Paylaşım İzinleri** seçeneği seçilir.<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_11-24.png" width=300>      
</p>

Açılan pencerede paylaşım hakkında aşağıdakiler yer alır:<br>
- Dosya yolu: Paylaşımın oluşturulduğu dizin 
- Kullanıcı: Paylaşımın sahibi olan kullanıcı ve yetkileri
- Grup: Paylaşımın sahibi olan grup ve yetkileri,
- Diğer: Diğer kullanıcıların yetkisi,
- Kullanıcıya İzin Ekle butonu: Paylaşıma erişim izni ve yetkileri verilecek kullanıcı eklemek için kullanılır.
- Gruba İzin Ekle butonu: Paylaşıma erişim izni ve yetkileri verilecek grup eklemek için kullanılır.
- Paylaşım İzinlerini Değiştir butonu: Kullanıcı, Grup ve Diğer için erişim yetkilerinin değiştirilmesi için kullanılır.
- Alt kısımdaki tablo: Paylaşım için yetki verilen kullanıcı ve gruplar yer alır.

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_11-29.png" width=600>      
</p>

### 2.4.1 Paylaşım İzinlerinin Değiştirilmesi
Paylaşım üzerindeki kullanıcı, grup ve diğer kullanıcıların yetkilerinin düzenlenmesi işlemidir. Bu işlem **Paylaşım İzinlerini Değiştir** butonu ile açılan pencerede gerçekleştirilir.<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_11-39.png" width=500>      
</p>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_11-40.png" width=500>      
</p>
Butona basıldıktan sonra gelen pencere şu şekildedir:<br>

Bu pencerede:<br>
- User = Kullanıcı (dosya sahibi) için Okuma-Yazma yetkilerini düzenler
- Group = Grup için Okuma-Yazma yetkilerini düzenler
- Other = Diğer kullanıcılar için Okuma-Yazma yetkilerini düzenler 
- Özyineli = Verilen veya alınan izinlerin, paylaşımın bulunduğu dizinin alt dizinleri içinde geçerli olmasını sağlar.

<br>
**Örnek: Paylaşımın Grup ve Diğer Kullanıcılar için Tüm Yetkilerinin Kaldırılması** <br>
Paylaşımın genel görünümü: <br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_11-46.png" width=500>      
</p>

İzinler penceresi:<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_11-47.png" width=300>      
</p>

İzinler penceresinden izinlerin değiştirilmesi:<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_11-48.png" width=300>      
</p>

Paylaşımın, izinler değiştirildikten sonraki genel görünümü:<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_11-49.png" width=500>      
</p>

### 2.4.2 Kullanıcıya İzin Ekleme
Paylaşıma kullanıcı atama ve yetkilendirme işlemidir. Bu işlem **Kullanıcıya İzin Ekle** butonu sayesinde gerçekleştirilir.<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_11-55.png" width=500>      
</p>

Butona basıldıktan sonra gelen pencere şu şekildedir:<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_12-41.png" width=600>      
</p>

Bu pencerede:<br>
- Kullanıcı kısmında yetki verilecek kullanıcı seçilir.
- Okuma seçeneği, seçilen kullanıcıya okuma (Read) yetkisi verir.
- Yazma seçeneği, seçilen kullanıcıya yazma (Write) yetkisi verir.
- Özyineli seçeneği, verilen yetkilerin paylaşımın alt dizinlerinde de geçerli olmasını sağlar.

<br>
Bir kullanıcı seçip istenilen yetkiler verildiğinde **Paylaşım İzinleri** penceresinin alt kısmındaki tabloda seçilmiş olan kullanıcı ve o kullanıcıya atanmış izinler görüntülenecektir.<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_12-48.png" width=600>      
</p>


### 2.4.3. Kullanıcı İznini Düzenleme
Bu işlem paylaşım üzerindeki kullanıcı izinlerini düzenleme işlemidir. Bunun için **Paylaşım İzinleri** penceresinin alt kısmındaki tabloda istenilen kullanıcıya sağ tıklanılır ve **Düzenle** seçeneği seçilir.<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_12-49.png" width=600>      
</p>

Daha sonra kullanıcıya istenilen izinler verilir veya çıkartılır. İzinler, özyineli olarak da verilebilir.<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_12-49-1.png" width=600>      
</p>

Düzenle butonu ile izinler kayıt edildiğinde, tabloda kullanıcının izinlerinin değişmiş olduğu gözükmektedir.<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_12-49-2.png" width=600>      
</p>

### 2.4.4. Kullanıcı İznini Silme
Paylaşımda yetkileri olan kullanıcının yetkilerinin silinmesi işlemidir. Bu işlem **Paylaşım İzinleri** penceresinin alt kısmındaki tabloda kullanıcıya sağ tıklayıp **Sil** ve **Özyineli Sil** işlemleri ile gerçekleştirilir.<br>

- Sil: Kullanıcının geçerli dizin üzerindeki yetkilerinin kaldırılması işlemidir.
- Özyineli Sil: Kullanıcının geçerli dizin ve tüm alt dizinlerindeki yetkilerinin kaldırılması işlemidir.

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_12-49-3.png" width=600>      
</p>

### 2.4.5. Gruba İzin Ekleme
Paylaşım için grup atama ve yetkilendirme işlemidir. Bu işlem **Gruba İzin Ekle** butonu sayesinde gerçekleştirilir.<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_12-50.png" width=600>      
</p>

Butona basıldıktan sonra karşılaşılan pencere aşağıdaki gibidir:<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_12-50_1.png" width=600>      
</p>

Bu pencerede:<br>
- Grup kısmında yetki verilecek grup seçilir.
- Okuma seçeneği, seçilen gruba okuma (Read) yetkisi verir.
- Yazma seçeneği, seçilen gruba yazma (Write) yetkisi verir.
- Özyineli seçeneği, verilen yetkilerin paylaşımın alt dizinlerinde de geçerli olmasını sağlar.

Bir grup seçip istenilen yetkiler verildiğinde **Paylaşım İzinleri** penceresinin alt kısmındaki tabloda seçilmiş olan grup ve o gruba atanmış izinler görüntülenecektir.<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-15_13-04.png" width=600>      
</p>

### 2.4.6. Grup İznini Düzenleme
Bu işlem paylaşım üzerindeki grubun izinlerini düzenleme işlemidir. Bunun için **Paylaşım İzinleri** penceresinin alt kısmındaki tabloda istenilen gruba sağ tıklanılır ve **Düzenle** seçeneği seçilir. <br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-16_08-22.png" width=600>      
</p>

Daha sonra gruba istenilen izinler verilir veya çıkartılır. İzinler, özyineli olarak da verilebilir.<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-16_08-26.png" width=600>      
</p>

Düzenle butonu ile izinler kayıt edildiğinde, tabloda grubun izinlerinin değişmiş olduğu gözükmektedir.<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-16_08-26_1.png" width=600>      
</p>

### 2.4.7. Grup İznini Silme
Paylaşımda yetkileri olan grubun yetkilerinin silinmesi işlemidir. Bu işlem **Paylaşım İzinleri** penceresinin alt kısmındaki tabloda gruba sağ tıklayıp **Sil** ve **Özyineli Sil** işlemleri ile gerçekleştirilir.<br>

- Sil: Grubun geçerli dizin üzerindeki yetkilerinin kaldırılması işlemidir.
- Özyineli Sil: Grubun geçerli dizin ve tüm alt dizinlerindeki yetkilerinin kaldırılması işlemidir.

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-16_08-32.png" width=600>      
</p>

## 2.5. Paylaşımın Boyutunun Ayarlanması
İstenilen paylaşım klasörünün ve alt klasörlerin boyutuna belirli bir kotanın koyulması işlemidir. Bu işlem eklenti arayüzünde paylaşıma sağ tıklayıp **Boyut Ayarla** seçeneği seçilerek gerçekleştirilir. <br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-16_08-46.png" width=300>      
</p>

Açılan pencerede paylaşımın referans gösterdiği dosyanın boyutu belirlenir ve **Ayarla** butonu ile kaydedilir.<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-16_08-48.png" width=600>      
</p>

Böylelikle paylaşımın adreslediği klasör bir kota kazanmış olur. Kullanıcılar ve gruplar bu klasör (ve alt klasörler) içerisinde dosya yükleme-oluşturma işlemlerinde belirlenmiş boyutu geçemez hale gelir.<br>

## 2.6. Paylaşımın Silinmesi
Kullanılmayan veya istenmeyen paylaşımın kaldırılması işlemidir. Bu işlem eklentinin arayüzünde seçilen paylaşıma sağ tıklayıp **Paylaşımı Sil** seçeneği ile gerçekleştirilir. <br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-16_08-54.png" width=600>      
</p>

Bu seçenek seçildiğinde onay penceresi gelir. Onay verildiğinde ise paylaşım silinmiş olur.<br>

<p align="center">
<img src="https://github.com/Toour/Sambafileshare-Guide/blob/main/Fileshare%20Fotolar/2021-09-16_09-16.png" width=600>      
</p>
