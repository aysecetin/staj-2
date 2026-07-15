# 🌞 16 Temmuz 2026 Perşembe


Bugün GPS destekli sürü yönetimi, hayvan pazarı ilanları ve veteriner iletişim özelliklerini bir araya getiren **SürüTakip** platformu üzerinde çalıştım. Projenin Next.js, TypeScript, PostgreSQL, Prisma ve Auth.js tabanlı yapısını kontrol ederek yerel geliştirme ortamını Docker üzerinden çalıştırdım.

Sistemde admin, sürü yöneticisi ve veteriner kullanıcıları için rol bazlı erişim yapısını düzenledim. Kullanıcıların yalnızca kendi yetkilerine uygun panellere ve verilere erişebilmesini sağladım. Sürü yöneticisi panelindeki hayvan, ürün, GPS takibi ve veteriner talebi bölümlerini geliştirdim. Ürün ekleme, düzenleme, silme ve fotoğraf yükleme işlemlerini veritabanına bağladım.

Ruhsatlı hayvan pazarlarının Excel dosyasından içe aktarılması üzerinde çalıştım. Excel sütunlarının okunması, hatalı kayıtların gösterilmesi, tekrar eden kayıtların engellenmesi ve adres bilgilerinden koordinat bulunması için gerekli yapıyı hazırladım. Bulunan pazarların Leaflet ve OpenStreetMap kullanılarak harita üzerinde gösterilmesini sağladım.

Veteriner talepleri için talep oluşturma, talep durumunu takip etme ve uygun veterinerlere yönlendirme iş akışlarını geliştirdim. GPS sistemini, ileride gerçek cihazlarla entegre edilebilmesi için servis tabanlı ve değiştirilebilir bir yapıda hazırladım. Şimdilik örnek konum, pil ve sinyal verileri üreten mock GPS sağlayıcısını kullandım.

Arayüz tarafında navbar geçişlerini, hover animasyonlarını, mobil uyumluluğu ve panel menülerini iyileştirdim. Bildirim simgesini işlevsel hale getirerek bildirimleri görüntüleme ve okundu olarak işaretleme özelliklerini ekledim. Kullanıcı profil simgesine açılır hesap menüsü ekleyerek profil sayfasına geçiş, ana siteye dönüş ve güvenli çıkış işlemlerini sağladım.

Çalışmalarımın sonunda projeyi test, lint, TypeScript ve production build kontrollerinden geçirdim. Gizli ortam değişkenlerinin GitHub'a yüklenmesini önlemek için `.gitignore` dosyasını düzenledim. 
