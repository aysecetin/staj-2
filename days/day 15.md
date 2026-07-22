# 🌞 22 Temmuz 2026 Çarşamba
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
