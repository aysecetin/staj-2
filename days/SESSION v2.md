# Color Gates Puzzle - UI & Progression Redesign (v2)

Bu güncelleme oyunun kullanıcı deneyimini modern mobil puzzle oyunları seviyesine çıkarmayı amaçlamaktadır.

Bu dokümandaki maddeler tasarım önerisi değildir. Uygulanması istenen gereksinimlerdir.

---

# 1. Oyun Adı

Uygulamanın resmi adı artık:

**Color Gates Puzzle**

olacaktır.

Eski "Renk Kapıları" başlığı tamamen kaldırılacaktır.

Logo olarak proje içerisinde bulunan yeni logo kullanılacaktır.

---

# 2. Açılış Akışı

Uygulama açıldığında artık ana menü gösterilmeyecektir.

Aşağıdaki ekranlar sırasıyla açılacaktır.

Splash Screen

↓

Bölüm Haritası

Oyuncu "Oyna" butonuna basmak zorunda kalmadan doğrudan mevcut bölümüne devam edebilmelidir.

---

# 3. Bölüm Haritası

Bölüm haritası tamamen yeniden tasarlanacaktır.

## Genel Kurallar

- Yol yatay olmayacaktır.
- Yol dikey olacaktır.
- Oyuncu yukarı doğru ilerliyormuş hissi oluşmalıdır.
- Kamera mevcut bölümün üzerinde başlamalıdır.

---

## Görünen Bölümler

Tamamlanan bölümler gösterilmeyecektir.

Örneğin oyuncu 48. bölümdeyse ekranda aşağıdakine benzer görünüm olmalıdır.

48

49 🔒

50 🔒

51 🔒

Daha eski bölümler haritada görünmeyecektir.

---

## Bölüm Kutuları

Kutuların üzerinde

Level 48

veya

Bölüm 48

yazmayacaktır.

Yalnızca sayı gösterilecektir.

Örneğin;

48

---

## Bölüm Önizlemesi

Mevcut bölüm kartında bulunan

- önizleme resmi
- ödül kartı
- hedef bilgisi

tamamen kaldırılacaktır.

Harita sade olacaktır.

---

# 4. Oyun Tahtası

Oyun tahtası artık sabit 6x6 değildir.

Desteklenmesi gereken boyutlar örnek olarak;

- 5x5
- 6x6
- 6x7
- 7x7
- 7x8
- 8x8

Tahta boyutu bölüm ihtiyacına göre değişebilmelidir.

---

## Girintili Tahtalar

Tahtalar tam dikdörtgen olmak zorunda değildir.

Void hücreleri kullanılarak;

- girintili
- çıkıntılı
- asimetrik

tahtalar oluşturulabilmelidir.

Bu sistem bölüm üreticisi tarafından desteklenmelidir.

---

# 5. Profil Sistemi

Haritanın sol üst köşesinde profil butonu bulunacaktır.

Profil ekranında;

- Avatar
- Profil Çerçevesi
- Oyuncu Seviyesi
- Tamamlanan Bölüm
- Toplam Altın

gösterilecektir.

---

## Avatar

Oyuncu avatarını değiştirebilir.

Yeni avatarlar;

- görevlerden
- etkinliklerden
- başarımlardan

kazanılabilir.

---

## Profil Çerçevesi

Avatar çerçevesi ayrı olarak değiştirilebilir.

Çerçeveler ödül sistemiyle açılır.

---

# 6. Google ile İlerleme Kaydı

Profil ekranına

Google ile ilerlemeni kaydet

özelliği eklenecektir.

Google hesabı bağlanırsa;

- bölüm ilerlemesi
- avatar
- çerçeve
- görevler
- güçlendiriciler
- ayarlar

bulutta saklanacaktır.

Google hesabı kullanılmıyorsa yerel kayıt kullanılacaktır.

---

# 7. Yerel Kayıt Sistemi

Oyun kapatıldığında aşağıdaki bilgiler kaydedilmelidir.

- Son oynanan bölüm
- Açılan bölümler
- Görev ilerlemeleri
- Güçlendirici sayıları
- Altın miktarı
- Avatar
- Çerçeve
- Ayarlar
- Dil

Oyuncu uygulamayı tekrar açtığında kaldığı yerden devam etmelidir.

---

# 8. Ayarlar

Ayarlar ekranına aşağıdakiler eklenecektir.

- Ses
- Müzik
- Titreşim
- Dil
- Google Hesabı
- Verileri Sıfırla

---

# 9. Dil Sistemi

Çoklu dil desteği eklenecektir.

Başlangıçta;

- Türkçe
- English

yeterlidir.

Yeni diller kolayca eklenebilecek şekilde yapı kurulmalıdır.

---

# 10. Görev Sistemi

Görev ekranı eklenecektir.

Oyuncu bölüm kazandıkça görevler ilerlemelidir.

Örnek görevler;

- 5 bölüm tamamla
- 20 bölüm tamamla
- 100 parça çıkar
- 10 sandık aç
- 500 saniye oyna

Görev tamamlandığında ödül alınabilir olmalıdır.

---

# 11. Başarımlar

Başarımlar sistemi eklenecektir.

Örnek;

- İlk Bölüm
- 10 Bölüm
- 50 Bölüm
- 100 Sandık
- 1000 Parça

---

# 12. Treasure Turtle

Domuz kumbara kullanılmayacaktır.

Yerine oyunun maskotu olacak bir karakter eklenecektir.

Adı:

Treasure Turtle

---

## Treasure Turtle Görevi

Treasure Turtle oyuncunun kazandığı altınları biriktirir.

Belirli miktara ulaştığında oyuncu ödülünü alabilir.

---

## Tasarım

Karakter;

- sevimli
- büyük gözlü
- premium
- 3D
- parlak plastik görünümlü

olmalıdır.

Kabuk kısmı LEGO bloklarından oluşmalıdır.

---

## Animasyonlar

Boşken;

- nefes alır
- göz kırpar

Altın geldikçe;

- kabuğu parlar
- altın sesi çıkar

Dolunca;

- sallanır
- oyuncuya gülümser
- ödül alınabilir hale gelir

---

# 13. Alt Menü

Alt navigasyon sadeleştirilecektir.

Bulunacak sekmeler;

- Profil
- Görevler
- Etkinlikler
- Mağaza

Ana Sayfa sekmesi olmayacaktır.

Bölüm haritası zaten ana ekran olacaktır.

---

# 14. Tasarım Hedefi

Arayüz;

- modern
- temiz
- premium
- canlı
- okunabilir

olmalıdır.

Candy Crush veya Royal Match kopyalanmamalıdır.

Kendi görsel kimliğini oluşturan, LEGO temalı, renkli ve premium bir tasarım dili kullanılmalıdır.

---

# 15. Referans Görseller

Bu geliştirmelerde sağlanan referans görseller kullanılacaktır.

Özellikle;

- dikey bölüm yolu
- girintili oyun tahtaları
- görev ekranı
- yeni logo

tasarım referansı olarak dikkate alınmalıdır.

Referansların birebir kopyalanması değil, aynı kalite seviyesinde özgün bir tasarım oluşturulması hedeflenmelidir.
