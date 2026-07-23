
# 🌞 21 Temmuz 2026 Salı 


Bugün Django ile geliştirilen kurumsal tedarik web sitesi üzerinde arayüz geliştirme, kullanıcı deneyimi iyileştirmeleri ve yönetim paneli düzenlemeleri gerçekleştirdim. Çalışmalar sırasında hem masaüstü hem de mobil cihazlarda daha modern, kurumsal ve kullanışlı bir görünüm elde etmeye odaklandım.

İlk olarak **İletişim** sayfasını yeniden düzenledim. Sayfada bulunan **Mesaj Gönder** formunu kaldırarak iletişim bilgilerinin daha sade ve doğrudan erişilebilir olmasını sağladım. İletişim bilgileri bölümünü daha geniş ve düzenli görünecek şekilde yeniden tasarladım. Telefon, WhatsApp, Instagram ve Trendyol bilgileri için kullanıcıların tek tıklamayla ilgili platformlara ulaşabileceği bağlantı kartları oluşturdum. Kartlara ilgili platformları temsil eden ikonlar ekledim ve her kartı platformun kurumsal renklerine uygun olarak tasarladım. WhatsApp kartında yeşil tonlarını, Trendyol kartında turuncu renkleri ve Instagram kartında platformun renk geçişlerini kullanarak görsel bütünlüğü artırdım.

İletişim kartlarının yerleşimini responsive yapıya uygun şekilde düzenledim. Kartların masaüstü cihazlarda iki sütun, mobil cihazlarda ise tek sütun olarak görüntülenmesini sağlayarak farklı ekran boyutlarında daha iyi bir kullanıcı deneyimi sundum. Kartlar arasındaki boşlukları ve hizalamaları düzenleyerek içeriklerin daha okunabilir olmasını sağladım.

Site genelinde kullanıcı deneyimini geliştirmek amacıyla navigasyon bölümünde de çeşitli iyileştirmeler yaptım.

**Yapılan Düzenlemeler**

- Menü çubuğunu sayfa kaydırıldığında ekranın üst kısmında sabit kalacak şekilde düzenledim.
- Menü bağlantılarına hover sırasında görünen hareketli alt çizgi efekti ekledim.
- Kullanıcının bulunduğu sayfanın menü üzerinde aktif olarak görüntülenmesini sağladım.
- Sayfalar arasında geçişlerde hafif giriş animasyonları ekledim.
- Hareket azaltma (`prefers-reduced-motion`) ayarı kullanan cihazlarda animasyonların otomatik olarak devre dışı bırakılmasını sağlayarak erişilebilirlik standartlarına uygun düzenlemeler yaptım.

Footer bölümünü de yeniden düzenleyerek daha profesyonel ve kurumsal bir görünüm kazandırdım.

**Footer Geliştirmeleri**

- Firma logosunu footer alanına ekledim.
- Firma hakkında kısa bir tanıtım metni oluşturdum.
- Kullanıcıların önemli sayfalara kolay ulaşabilmesi için hızlı bağlantılar menüsü hazırladım.
- Telefon, e-posta ve adres bilgilerini ikonlarla birlikte düzenli şekilde yerleştirdim.
- Instagram ve Trendyol hesaplarına yönlendiren sosyal medya butonları ekledim.
- Telif hakkı metninde yıl bilgisinin otomatik olarak güncellenmesini sağlayan dinamik yapı oluşturdum.
- Header, footer ve iletişim sayfasının tüm mobil cihazlarda sorunsuz çalışması için responsive CSS düzenlemeleri gerçekleştirdim.

Arayüz çalışmalarının ardından yönetim paneli tarafında da geliştirmeler yaptım.

**Django Tarafında Yapılan Çalışmalar**

- Site ve Django yönetim panelinde ALTINER logosunun kullanılmasını sağladım.
- Site ayarları modeline **Trendyol mağaza bağlantısı** alanı ekledim.
- Trendyol bağlantısının Django yönetim paneli üzerinden değiştirilebilmesini sağladım.
- Model değişikliği için gerekli migration dosyalarını oluşturdum.
- CSS dosyalarının tarayıcı önbelleğinde eski sürümlerinin kullanılmasını önlemek amacıyla sürüm parametrelerini güncelledim.

Çalışmaların tamamlanmasının ardından sistem kontrollerini gerçekleştirerek projenin sorunsuz çalıştığını doğruladım.

**Kontrol ve Yayınlama**

- Django sistem kontrollerini (`check`) çalıştırarak herhangi bir yapılandırma hatası bulunmadığını doğruladım.
- Migration durumunu kontrol ederek eksik veya uygulanmamış veritabanı değişikliği olmadığını doğruladım.
- Yaptığım tüm değişiklikleri Git ile commitledim.
- Projenin güncel sürümünü GitHub üzerindeki **aysecetin/kurumsal-tedarik-django** deposunun **main** branch'ine başarıyla gönderdim.
