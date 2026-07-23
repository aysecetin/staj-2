
# 🌞 21 Temmuz 2026 Salı

Bugün Django ile geliştirilen kurumsal tedarik web sitesi üzerinde arayüz geliştirme, kullanıcı deneyimi iyileştirmeleri ve yönetim paneli düzenlemeleri gerçekleştirdim. Çalışmalar sırasında hem masaüstü hem de mobil cihazlarda daha modern, kurumsal ve kullanışlı bir görünüm elde etmeye odaklandım.

İlk olarak İletişim sayfasını yeniden düzenledim. Sayfada bulunan Mesaj Gönder formunu kaldırarak iletişim bilgilerinin daha sade ve doğrudan erişilebilir olmasını sağladım. İletişim bilgileri bölümünü yeniden tasarlayarak daha geniş bir yerleşim oluşturup okunabilirliği artırdım. Telefon, WhatsApp, Instagram ve Trendyol bilgileri için kullanıcıların tek tıklamayla ilgili platformlara ulaşabileceği bağlantı kartları hazırladım. Kartlara platformları temsil eden ikonlar ekledim ve her kartı kendi kurumsal renklerine uygun şekilde tasarladım. Özellikle WhatsApp kartında yeşil tonları, Trendyol kartında turuncu renkler ve Instagram kartında platformun renk geçişlerini kullanarak görsel bütünlük oluşturdum.

İletişim kartlarının yerleşimini responsive yapıya uygun şekilde düzenledim. Masaüstü ekranlarda iki sütun halinde görüntülenmesini, mobil cihazlarda ise tek sütun düzenine geçmesini sağlayarak farklı ekran boyutlarında kullanıcı deneyimini iyileştirdim. Kartlar arasındaki boşlukları ve hizalamaları yeniden düzenleyerek içeriklerin daha rahat okunmasını sağladım.

Site genelinde kullanıcı deneyimini geliştirmek amacıyla navigasyon bölümünde de çeşitli iyileştirmeler yaptım.

Menü çubuğunu sayfa kaydırıldığında ekranın üst kısmında sabit kalacak şekilde düzenledim.
Menü bağlantılarına hover sırasında görünen hareketli alt çizgi animasyonu ekledim.
Kullanıcının bulunduğu sayfanın menü üzerinde aktif olarak görüntülenmesini sağladım.
Sayfalar arasında geçişlerde hafif giriş animasyonları ekledim.
Hareket azaltma (prefers-reduced-motion) ayarı kullanan cihazlarda bu animasyonların otomatik olarak devre dışı bırakılmasını sağlayarak erişilebilirlik standartlarına uygun düzenlemeler yaptım.

Footer bölümünü de tamamen yeniden düzenleyerek daha profesyonel ve kurumsal bir görünüm kazandırdım. Bu kapsamda;

Firma logosunu footer alanına ekledim.
Firma hakkında kısa bir açıklama metni oluşturdum.
Kullanıcıların önemli sayfalara kolay ulaşabilmesi için hızlı bağlantılar menüsü hazırladım.
Telefon, e-posta ve adres bilgilerini ikonlarla birlikte düzenli şekilde yerleştirdim.
Instagram ve Trendyol hesaplarına yönlendiren sosyal medya butonları ekledim.
Telif hakkı metninde yıl bilgisinin otomatik güncellenmesini sağlayan dinamik yapı oluşturdum.

Arayüz düzenlemelerinin ardından yönetim panelinde de bazı geliştirmeler gerçekleştirdim. Site ayarları modeline Trendyol mağaza bağlantısı alanını ekleyerek bu bilginin Django yönetim panelinden kolayca değiştirilebilmesini sağladım. Model değişikliği sonrasında gerekli migration dosyalarını oluşturdum ve veritabanına uygulanabilirliğini kontrol ettim.

Ayrıca hem web sitesinde hem de Django yönetim panelinde ALTINER firmasına ait logonun kullanılmasını sağlayarak kurumsal kimlik bütünlüğünü güçlendirdim. CSS dosyalarının tarayıcı önbelleğinde eski sürümlerinin kullanılmasını önlemek amacıyla statik dosya sürüm parametrelerini güncelledim.

Çalışmaların tamamlanmasının ardından projenin sorunsuz çalıştığını doğrulamak amacıyla Django sistem kontrollerini çalıştırdım ve herhangi bir yapılandırma hatası bulunmadığını kontrol ettim. Migration durumunu tekrar inceleyerek eksik veya uygulanmamış veritabanı değişikliği olmadığını doğruladım. Son olarak yaptığım tüm geliştirmeleri Git ile commitledim ve projenin güncel sürümünü GitHub üzerindeki aysecetin/kurumsal-tedarik-django deposunun main branch'ine başarıyla gönderdim.
