
# 🌞 28 Temmuz 2026 Salı

# Altıner Toptan Web Sitesine İkinci Telefon Numarası Desteğinin Eklenmesi

### Yapılan Çalışmanın Amacı

Bugün, **Altıner Toptan** (**altınertoptan.com**) kurumsal tedarik web sitesinin iletişim altyapısını geliştirerek yönetim panelinden kontrol edilebilen ikinci telefon numarası desteği ekledim. Böylece firma, ihtiyaç duyduğunda birden fazla telefon numarasını ziyaretçilere sunabilecek ve tüm iletişim bilgilerini tek bir panel üzerinden yönetebilecek hale geldi.

---

### Mevcut Yapının İncelenmesi

- Projede iletişim bilgilerinin tutulduğu yapıyı inceledim.
- Telefon bilgilerinin **SiteSetting** modeli üzerinden yönetildiğini tespit ettim.
- Yeni özelliği mevcut yapıya uygun şekilde geliştirmeye karar verdim.

---

### Veritabanı ve Model Güncellemesi

- **secondary_phone** adında yeni bir alan ekledim.
- İkinci telefon numarası alanını isteğe bağlı (opsiyonel) olarak tanımladım.
- İkinci telefon numarası girilmediğinde sitede boş bir telefon kartının görüntülenmesini engelledim.
- Model değişikliğini veritabanına uygulamak için **0007_sitesetting_secondary_phone.py** isimli migration dosyasını oluşturdum.

---

### Yönetim Panelinin Güncellenmesi

- Django yönetim panelindeki **Site Ayarları** bölümünü güncelledim.
- İkinci telefon numarasının yönetim panelinden eklenebilmesini ve düzenlenebilmesini sağladım.
- Böylece yeni telefon numarasının kod değişikliği yapılmadan yönetilebilmesini sağladım.

---

### İletişim Sayfasının Düzenlenmesi

- İletişim sayfasındaki telefon kartlarını yeniden düzenledim.
- İkinci telefon numarası girildiğinde mevcut telefon numarasının yanında veya altında ayrı bir iletişim seçeneği olarak gösterilmesini sağladım.
- İkinci telefon numarası girilmediğinde ilgili alanın otomatik olarak gizlenmesini sağlayarak arayüzün düzenli görünmesini sağladım.

---

## Footer Bölümünün Güncellenmesi

- Footer bölümündeki iletişim alanını güncelledim.
- İkinci telefon numarasının sayfanın alt kısmında da görüntülenmesini sağladım.
- Telefon numaralarının tıklanabilir bağlantılar olarak çalışmasını sağladım.

---

## Telefon Bağlantılarının Düzenlenmesi

- Telefon numaralarının bağlantılarda sorunsuz çalışabilmesi için numaraların içerisindeki boşlukları ve özel karakterleri temizleyen bir yapı hazırladım.
- Böylece ziyaretçiler telefon numarasına tıkladığında cihazın telefon uygulamasının doğrudan açılmasını sağladım.

---

## Test ve Doğrulama

- Geliştirdiğim özellik için gerekli testleri ekledim.
- İkinci telefon numarası bulunduğunda iletişim sayfasında doğru şekilde görüntülendiğini doğruladım.
- Footer bölümünde de ikinci telefon numarasının başarılı şekilde gösterildiğini kontrol ettim.

---

## Yayınlama Süreci

- Yaptığım değişiklikleri Git ile **"İkinci telefon desteği ekle"** açıklamasıyla kaydettim.
- Güncellemeleri GitHub üzerindeki **main** dalına gönderdim.
- Sunucuya bağlanarak güncel kodları **git pull origin main** komutuyla çektim.
- İşlem öncesinde olası bir veri kaybına karşı mevcut SQLite veritabanının yedeğini aldım.
- **python manage.py migrate** komutunu çalıştırarak yeni veritabanı alanını oluşturdum.
- **python manage.py check** komutunu kullanarak projede herhangi bir yapılandırma veya sistem hatası bulunmadığını doğruladım.
- Son olarak Gunicorn uygulama sunucusunu yeniden yükleyerek değişiklikleri hizmet kesintisi oluşturmadan canlı ortama aktardım.

---

## Elde Edilen Sonuç

Bu çalışma sonucunda **altınertoptan.com** web sitesine yönetim paneli üzerinden kontrol edilebilen, isteğe bağlı olarak kullanılabilen ve tıklanabilir bağlantılarla çalışan ikinci telefon numarası desteği kazandırdım. Böylece firmanın ziyaretçilere birden fazla iletişim numarası sunabilmesi sağlanırken, sistemin yönetilebilirliği ve kullanıcı deneyimi de geliştirilmiş oldu.



