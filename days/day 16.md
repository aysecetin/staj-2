# 23 Temmuz 2026 Perşembe
Bugün Altıner Toptan kurumsal web sitesinin canlı yayın ortamına alınması ve son kontrolleri üzerinde çalıştım. Alan adı, sunucu ve uygulama tarafındaki eksiklikleri gidererek projenin yayın sürecini tamamladım.

Yaptığım çalışmalar:

- Alan adının uluslararası karakter (IDN/Punycode) yapısını inceleyerek DNS ve SSL yapılandırmalarını buna uygun şekilde düzenledim.
- CloudPanel üzerinden site yapılandırmalarını kontrol ederek SSL sertifikasının doğru şekilde çalışmasını sağladım.
- GitHub deposundaki Django projesini sunucuya aktararak gerekli dosyaları canlı ortama taşıdım.
- Python sanal ortamını (Virtual Environment) oluşturdum ve proje bağımlılıklarını yükledim.
- Sunucudaki Python sürümünü güncelleyerek Django 6 sürümüyle uyumlu hale getirdim.
- Ortam değişkenlerini (.env) oluşturarak güvenlik ayarlarını yapılandırdım. Debug modunu kapattım, SSL yönlendirmelerini ve güvenli çerez ayarlarını aktif hale getirdim.
- Django veritabanı migration işlemlerini gerçekleştirerek gerekli tabloları oluşturdum.
- ```collectstatic``` komutunu çalıştırarak statik dosyaları sunucuya aktardım.
- Gunicorn yapılandırmasını hazırlayarak uygulamanın servis olarak çalışmasını sağladım.
- Nginx yapılandırmasını düzenleyerek Gunicorn ile ters vekil (Reverse Proxy) bağlantısını kurdum.
- Statik dosyaların doğru şekilde sunulabilmesi için /static ve /media yönlendirmelerini yapılandırdım.
- Django yönetim panelinin (Admin Panel) çalışmasını test ederek gerekli kullanıcı hesaplarını oluşturdum.
- Google Maps iframe bağlantısının uzun URL nedeniyle veritabanında kesildiğini tespit ettim.
- Harita URL alanının karakter sınırını artırmak amacıyla model üzerinde düzenleme yaparak yeni migration oluşturdum ve canlı sunucuya uyguladım.
- Google Maps entegrasyonunu yeniden yapılandırarak iletişim sayfasındaki haritanın sorunsuz görüntülenmesini sağladım.
- Siteye favicon (sekme ikonu) desteği ekledim, gerekli ikon dosyalarını oluşturarak tüm sayfalarda kullanılacak şekilde yapılandırdım.
- Favicon değişikliklerini GitHub üzerinden sunucuya aktararak statik dosyaları yeniden yayınladım ve tarayıcı önbelleği kontrollerini gerçekleştirdim.
- Canlı ortam üzerinde iletişim bilgileri, sosyal medya bağlantıları, görseller ve genel site işlevlerini test ederek son kontrolleri tamamladım.

www.altınertoptan.com
