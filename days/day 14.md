
# 21 Temmuz 2026 Salı
Django ile geliştirilen kurumsal tedarik web sitesi üzerinde arayüz düzenlemeleri yaptım.

İletişim sayfasında bulunan Mesaj Gönder formunu tamamen kaldırdım.

İletişim bilgileri bölümünü sayfada daha geniş ve düzenli görünecek şekilde yeniden tasarladım.

Telefon, Trendyol, WhatsApp ve Instagram bilgileri için ayrı bağlantı kartları oluşturdum.

Kartlara ilgili platformları temsil eden ikonlar ekledim.

WhatsApp kartını yeşil, Instagram kartını platformun renklerine uygun, Trendyol kartını ise turuncu renkte tasarladım.

İletişim kartları arasındaki boşlukları düzenleyerek bilgilerin daha kolay okunmasını sağladım.

Kartların masaüstünde iki sütun, mobil cihazlarda ise tek sütun şeklinde görünmesini sağladım.

Navigasyon menüsünü sayfa kaydırıldığında üst bölümde sabit kalacak şekilde düzenledim.

Menü bağlantılarına hover sırasında görünen hareketli alt çizgi efekti ekledim.

Kullanıcının bulunduğu sayfanın menüde aktif olarak gösterilmesini sağladım.

Sayfalar arasında geçiş yapılırken hafif bir giriş animasyonu ekledim.

Hareket azaltma ayarı kullanan cihazlar için animasyonları otomatik olarak devre dışı bıraktım.

Footer bölümünü daha profesyonel ve kurumsal bir görünüme kavuşturdum.

Footer içerisine firma logosu ve kısa firma açıklaması ekledim.

Footer bölümüne hızlı bağlantılar menüsü oluşturdum.

Telefon, e-posta ve adres bilgilerini ikonlu şekilde footer alanına ekledim.

Instagram ve Trendyol bağlantıları için ayrı sosyal medya butonları hazırladım.

Footer bölümüne güncel yılı otomatik gösteren telif hakkı metni ekledim.

Header, footer ve iletişim sayfasının mobil cihazlarla uyumlu çalışması için responsive CSS düzenlemeleri yaptım.

Site ve Django yönetim panelinde ALTINER logosunun kullanılmasını sağladım.

Site ayarları modeline Trendyol mağaza bağlantısı alanı ekledim.

Trendyol bağlantısının Django yönetim panelinden değiştirilebilmesini sağladım.

Model değişikliği için gerekli migration dosyasını oluşturdum.

CSS dosyalarının tarayıcı önbelleğinde eski hâliyle kalmaması için sürüm parametrelerini güncelledim.

Django sistem kontrollerini çalıştırarak projede yapılandırma hatası olmadığını doğruladım.

Migration kontrolü yaparak eksik veritabanı değişikliği bulunmadığını doğruladım.

Yaptığım değişiklikleri Git ile commitledim.

Projenin güncel hâlini GitHub üzerindeki aysecetin/kurumsal-tedarik-django deposunun main branch’ine gönderdim.
Bugün geliştirdiğim Django tabanlı web projesini canlı ortama taşımak amacıyla sunucu ve alan adı altyapısı üzerinde çalışmalar yaptım.

Çalışmalar kapsamında;

- Proje için altinertoptan.com alan adını satın aldım.
- Alan adının kayıt işlemlerini tamamlayarak DNS yönetim ekranını inceledim.
- Canlı yayın sürecinde kullanılacak alan adı yönlendirmeleri ve DNS yapılandırmaları hakkında gerekli hazırlıkları yaptım.
- DeHost üzerinden projeye ait yeni bir VPS (Virtual Private Server) oluşturdum.
- Sunucu bilgilerini kontrol ederek SSH bağlantısı üzerinden Ubuntu sunucusuna erişim sağladım.
- Sunucu üzerinde sistem paketlerini güncelleyerek CloudPanel kurulumu için gerekli ön hazırlıkları gerçekleştirdim.
- CloudPanel kurulumu sırasında oluşan paket ve veritabanı hatalarını inceleyerek hata kayıtlarını analiz ettim.
- Yarım kalan paket kurulumlarını ve sistem servislerini kontrol ederek problemin kaynağını araştırdım.
- Daha sağlıklı bir kurulum gerçekleştirebilmek amacıyla sunucuyu sıfırlayarak Ubuntu 22.04 işletim sistemini yeniden kurdum.
- Yeni kurulum sonrasında SSH bağlantısını tekrar yapılandırarak sunucu erişim testlerini gerçekleştirdim.
- Sunucuya erişim problemi yaşanması üzerine farklı internet bağlantıları (ev interneti ve mobil internet) üzerinden SSH bağlantı testleri yaptım.
- Ping ve ağ erişim testleri gerçekleştirerek bağlantı probleminin istemci bilgisayardan mı yoksa sunucu taraflı mı olduğunu analiz ettim.
- SSH anahtarlarını yenileyerek bağlantı doğrulama işlemlerini tekrar gerçekleştirdim.
- Yapılan testler sonucunda problemin sunucu tarafındaki ağ yapılandırması ile ilgili olabileceğini değerlendirdim. Durumu ekip arkadaşım ile birlikte inceleyerek gerekli kontrolleri gerçekleştirdik. Yapılan incelemeler sonrasında sunucu tarafındaki erişim problemi giderildi ve bağlantı yeniden sağlandı. Böylece canlı yayın sürecine devam edebilmek için gerekli sunucu altyapısını hazır hale getirdim.
