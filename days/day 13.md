# 🌞 20 Temmuz 2026 Pazartesi

Bugün PRO YILDIZ Güvenlik Sistemleri projesinin Django sürümünü canlı sunucuya yayınlamak için çalıştım. İlk olarak Ubuntu tabanlı VPS sunucusuna CloudPanel kurulumunu yaptım ve Python uygulamalarını çalıştırabilecek hosting ortamını hazırladım. Daha sonra CloudPanel üzerinden yeni bir Python sitesi oluşturarak Python 3.12 sürümünü ve uygulamanın çalışacağı port ayarlarını yapılandırdım.

GitHub üzerindeki projenin django-gecis dalını sunucuya klonladım. Sanal Python ortamını (virtual environment) oluşturarak etkinleştirdim ve requirements.txt dosyasında bulunan tüm gerekli kütüphaneleri kurdum. Django projesini çalıştırarak ilk sistem kontrollerini gerçekleştirdim.

Alan adının sunucuya yönlendirilmesi için METUnic DNS paneline girerek A kayıtlarını düzenledim. Ana alan adını, www alt alan adını ve mail.nedenkapatilsin.com.tr adresini sunucunun IP adresine yönlendirdim. DNS kayıtlarının aktif olmasının ardından CloudPanel üzerinden Let's Encrypt SSL sertifikasını oluşturarak HTTPS bağlantısını aktif hale getirdim.

Projenin .env dosyasını düzenleyerek ALLOWED_HOSTS, CSRF_TRUSTED_ORIGINS ve SMTP e-posta ayarlarını yapılandırdım. Daha sonra collectstatic komutunu çalıştırarak statik dosyaları tek dizinde topladım. Nginx yapılandırmasını düzenleyerek CSS, JavaScript ve görsel dosyalarının doğru şekilde yayınlanmasını sağladım.

Yayınlama sırasında karşılaştığım DisallowedHost, SSL doğrulama, statik dosyaların yüklenmemesi (404), Nginx yönlendirme ve yapılandırma hatalarını tek tek inceleyerek gerekli düzenlemeleri yaptım. Django yönetim paneli için superuser oluşturarak yönetim paneline giriş testlerini gerçekleştirdim.

Son olarak sipariş oluşturma özelliğini test ettim. Test sırasında ön yüzde kullanılan ürün kimlikleri ile Django veritabanındaki UUID tabanlı ürün kimlikleri arasında uyumsuzluk olduğunu tespit ettim. Hatanın kaynağını analiz ederek çözüm için gerekli düzenlemeleri planladım. Böylece Django projesini canlı sunucu ortamında çalışır hale getirerek yayınlama sürecini büyük ölçüde tamamladım.
