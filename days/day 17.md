# 🌞 24 Temmuz 2026 Cuma


**SürüTakip Mobil Uygulamasında Güvenlik ve Yayınlama Çalışmaları**

Bugün SürüTakip projesinin mobil uygulama geliştirme sürecine devam ettim. İlk olarak mobil uygulamanın güvenlik ve gizlilik gereksinimlerini ele aldım. Django REST API üzerinde oturum açma ve token yenileme işlemlerine hız sınırı ekleyerek kısa süre içerisinde çok fazla başarısız istek gönderilmesini engelleyecek bir yapı oluşturdum. Üretim ortamı için HTTPS yönlendirmesi, güvenli çerez kullanımı, HSTS, güvenli gizli anahtar kontrolü ve yönlendirme güvenliği gibi ayarları yapılandırdım.  

Kullanıcıların kişisel verileri üzerindeki kontrolünü artırmak amacıyla hesap silme özelliği geliştirdim. Bu işlemde yanlışlıkla hesap silinmesini önlemek için kullanıcının mevcut şifresini ve özel bir onay metnini girmesini zorunlu hale getirdim. Hesap silindiğinde kullanıcıyla ilişkili hayvan, GPS cihazı, veteriner talebi, bildirim ve abonelik gibi kayıtların da uygun şekilde kaldırılmasını sağladım. Mobil uygulamaya gizlilik bilgilerini görüntüleme ve hesabı silme ekranları ekledim.  
  
Uygulamanın mağaza yayın sürecine hazırlanması kapsamında gizlilik politikası taslağı, hesap silme bilgilendirme sayfası, mağaza veri beyanı çalışma belgesi ve yayın güvenliği kontrol listesi hazırladım. Böylece Google Play Data Safety ve App Store gizlilik bölümlerinde kullanılacak bilgileri proje içerisinde dokümante ettim.  

Push bildirim özelliği için hem mobil uygulama hem de Django sunucu tarafında gerekli altyapıyı geliştirdim. Mobil uygulamanın gerçek cihazı kaydetmesini, kullanıcıdan bildirim izni istemesini ve Expo push token bilgisini Django API’ye göndermesini sağladım. Kullanıcı bir bildirime dokunduğunda bildirimin türüne göre ilgili hayvan, GPS veya veteriner talebi ekranına yönlendirme yapılacak şekilde navigasyon yapısını oluşturdum. Sunucu tarafında ise bekleyen bildirimleri Expo servisine gönderen ve bildirim teslimat sonuçlarını kontrol eden yönetim komutları hazırladım.

  
Expo mobil projesini EAS hesabına bağladım. Android ve iOS için development, preview ve production derleme profillerini yapılandırdım. Uygulama için EAS proje kimliği oluşturdum ve Android imzalama anahtarının Expo sunucusunda güvenli şekilde hazırlanmasını sağladım.  

Mobil uygulamanın gerçek cihazdan erişebilmesi için Django projesini canlı ortama taşıdım. Render üzerinde SürüTakip’e ait bir PostgreSQL veritabanı ve Django web servisi oluşturdum. Veritabanı bağlantısı, production ortam değişkenleri, migration işlemleri, statik dosya toplama işlemi ve Gunicorn başlangıç komutunu yapılandırdım. Render tarafından sağlanan HTTPS adresini Django’nun güvenilir host ve CSRF ayarlarına otomatik olarak ekledim.  

İlk yayın denemesinde Leaflet JavaScript dosyasının var olmayan bir kaynak haritasına referans vermesi nedeniyle statik dosya derleme hatasıyla karşılaştım. Render loglarını inceleyerek hatanın kaynağını tespit ettim. Kullanılmayan kaynak haritası referansını kaldırdıktan sonra production ortamında collectstatic işlemini yeniden test ettim. Düzeltmeyi GitHub’a gönderdikten sonra Render otomatik olarak yeni bir deploy başlattı ve Django uygulaması başarıyla canlı duruma geçti.  

Canlıya alınan API adresini Expo’nun preview ortamında EXPO_PUBLIC_API_URL değişkeni olarak tanımladım. Böylece Android preview sürümünün yerel bilgisayardaki adres yerine internete açık ve HTTPS kullanan Django API’ye bağlanmasını sağladım. Daha sonra Android APK oluşturmak için EAS Build işlemini başlattım. Proje dosyaları EAS sunucusuna başarıyla yüklendi ve Android derlemesi uzaktaki derleme kuyruğuna alındı.
Çalışmaların sonunda aşağıdaki kontrolleri gerçekleştirdim:

- 48 adet Django testini başarıyla çalıştırdım.
- Django üretim güvenliği kontrolünü hatasız tamamladım.
- TypeScript tip kontrolünü ve Expo lint işlemini çalıştırdım.
- Expo proje yapılandırmasını ve EAS proje bağlantısını doğruladım.
- Statik dosya derleme işlemini production ayarlarıyla test ettim.
- Git çalışma alanının temiz ve uzak GitHub branch’iyle eşit olduğunu kontrol ettim.
  
Yaptığım tüm değişiklikleri açıklayıcı commit mesajlarıyla GitHub’daki feature/mobile-foundation branch’ine gönderdim. Gün sonunda Django web servisini ve mobil API’yi canlı ortama taşımış, Expo preview ortamını canlı API’ye bağlamış ve gerçek cihazda kurulacak Android APK’nın derleme sürecini başlatmış oldum.










