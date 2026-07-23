# 🌞 24 Temmuz 2026 Cuma

Mobil Uygulama Güvenliği ve Canlı Ortam Çalışmaları
Bugün SürüTakip mobil uygulamasının güvenlik, gizlilik ve yayın altyapısı üzerinde çalıştım. Django REST API tarafında oturum açma ve token yenileme işlemlerine hız sınırları ekledim. Üretim ortamında güvenli çerez, HTTPS yönlendirmesi, HSTS ve güvenli gizli anahtar kullanımı gibi ayarları yapılandırdım.
Kullanıcıların hesaplarını uygulama içerisinden kalıcı olarak silebilmesi için şifre ve onay metniyle korunan hesap silme özelliğini geliştirdim. Ayrıca gizlilik politikası ve hesap silme bilgilendirme sayfalarını hazırladım. App Store ve Google Play için gerekli veri beyanı ile güvenlik kontrol dokümanlarını oluşturdum.
Mobil uygulamaya cihaz kaydı ve push bildirim altyapısı ekledim. Bildirim izninin yalnızca kullanıcı isteğiyle alınmasını sağladım. Bildirime dokunulduğunda ilgili hayvan, GPS veya veteriner sayfasına yönlendirme yapılacak şekilde düzenleme yaptım. Sunucu tarafında bildirim gönderme ve teslimat sonuçlarını kontrol etme komutlarını hazırladım.
Expo projesini EAS hesabına bağladım ve Android/iOS derleme profillerini yapılandırdım. Uygulamanın EAS proje kimliğini oluşturdum ve Android için güvenli imzalama anahtarı hazırladım.
Django projesini canlıya almak için Render üzerinde PostgreSQL veritabanı ve web servisi oluşturdum. Üretim ortam değişkenlerini, migration işlemlerini, statik dosya derlemesini ve HTTPS bağlantısını yapılandırdım. Statik Leaflet dosyasındaki eksik kaynak haritası referansından oluşan yayın hatasını tespit ederek giderdim. Düzeltmenin ardından Django sitesi başarıyla canlıya alındı.
Canlı API adresini Expo preview ortamına tanımladım. Android APK oluşturmak için EAS Build işlemini başlattım. Derleme işlemi EAS sunucusunda sıraya alındı ve gerçek cihaz testi için hazır hale getirilmeye başlandı.
Çalışmaların sonunda 48 Django testini, TypeScript kontrolünü, lint işlemini, Expo yapılandırmasını ve üretim güvenlik kontrollerini başarıyla tamamladım. Yaptığım değişiklikleri ayrı commitlerle GitHub’daki feature/mobile-foundation branch’ine gönderdim.


21:37


















Onay iste
