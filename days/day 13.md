# 🌞 20 Temmuz 2026 Pazartesi



Bugün PRO YILDIZ Güvenlik Sistemleri projesinin Django sürümünün canlı sunucuya yayınlanması üzerinde çalıştım. Öncelikle Ubuntu tabanlı VPS sunucusuna CloudPanel kurulumu yapılarak Python uygulamaları için gerekli hosting ortamı hazırlandı. CloudPanel üzerinden yeni bir Python sitesi oluşturuldu ve uygulama için Python 3.12 sürümü ile gerekli port ayarları yapılandırıldı.

Projenin GitHub deposundaki django-gecis dalı sunucuya klonlandı ve sanal Python ortamı (virtual environment) etkinleştirildi. Gerekli Python paketleri requirements.txt dosyası üzerinden kuruldu. Django projesi çalıştırılarak ilk sistem kontrolleri gerçekleştirildi.

Alan adının sunucuya yönlendirilmesi amacıyla METUnic DNS yönetim paneli üzerinden A kayıtları düzenlendi. Ana alan adı, www alt alan adı ve mail.nedenkapatilsin.com.tr alt alan adı sunucu IP adresine yönlendirildi. DNS kayıtlarının aktif hale gelmesinin ardından CloudPanel üzerinden Let's Encrypt SSL sertifikası oluşturularak HTTPS bağlantısı etkinleştirildi.

Django projesinde ortam değişkenleri (.env) düzenlenerek ALLOWED_HOSTS, CSRF_TRUSTED_ORIGINS ve SMTP e-posta ayarları yapılandırıldı. Uygulamanın statik dosyaları collectstatic komutu ile tek dizinde toplandı ve Nginx yapılandırması güncellenerek CSS, JavaScript ve görsel dosyalarının doğru şekilde sunulması sağlandı.

Yayınlama sürecinde oluşan DisallowedHost, SSL sertifikası, statik dosyaların yüklenmemesi (404), Nginx yönlendirme ve yapılandırma sorunları analiz edilerek gerekli düzenlemeler yapıldı. Ayrıca Django yönetim paneli için süper kullanıcı oluşturuldu ve yönetim paneline erişim test edildi.

Son olarak sipariş oluşturma işlemi test edildi. Testler sırasında ön yüzde kullanılan ürün kimlikleri ile Django veritabanındaki UUID tabanlı ürün kimlikleri arasında uyumsuzluk olduğu tespit edildi. Hatanın nedeni analiz edilerek çözüm için gerekli düzenleme planlandı. Böylece projenin canlı sunucu ortamına başarılı şekilde aktarılması sağlanırken, kalan uygulama geliştirme ve hata giderme çalışmaları için gerekli altyapı hazırlanmış oldu.
