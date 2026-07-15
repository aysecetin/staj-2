# 🌞 16 Temmuz 2026 Perşembe



Bugün **SürüTakip** platformu üzerinde çalıştım. Bu proje, büyükbaş ve küçükbaş hayvan yetiştiricilerinin sürülerini dijital ortamda yönetebilmesini sağlayan kapsamlı bir yönetim sistemidir.

**Projenin temel özellikleri:**
- **GPS destekli sürü takibi** ile hayvanların konum bilgilerinin görüntülenmesi.
- **Hayvan kayıt yönetimi** ile hayvan ekleme, düzenleme, silme ve detaylı bilgilerin tutulması.
- **Ürün yönetimi** ile yetiştiricilerin ürünlerini sisteme ekleyebilmesi ve yönetebilmesi.
- **Hayvan pazarı modülü** sayesinde satılık hayvan ilanlarının oluşturulması ve ruhsatlı hayvan pazarlarında yayınlanabilmesi.
- **Veteriner iletişim sistemi** ile veteriner talebi oluşturma, talepleri takip etme ve uygun veterinerlere yönlendirme.
- **Rol bazlı kullanıcı sistemi** ile admin, sürü yöneticisi ve veteriner kullanıcılarının farklı yetkilere sahip olması.
- **Harita entegrasyonu** sayesinde hayvan pazarlarının ve GPS verilerinin harita üzerinde görüntülenebilmesi.

Çalışmalarım kapsamında projenin Next.js, TypeScript, PostgreSQL, Prisma ve Auth.js tabanlı altyapısını kontrol ederek yerel geliştirme ortamını Docker üzerinden çalıştırdım.

Admin, sürü yöneticisi ve veteriner kullanıcıları için rol bazlı erişim yapısını düzenledim. Kullanıcıların yalnızca kendi yetkilerine uygun sayfalara ve verilere erişebilmesini sağladım. Sürü yöneticisi panelindeki hayvan, ürün, GPS takibi ve veteriner talebi bölümlerini geliştirdim. Ürün ekleme, düzenleme, silme ve fotoğraf yükleme işlemlerini veritabanı ile entegre ettim.

Hayvan pazarı modülü için ruhsatlı hayvan pazarlarının Excel dosyasından sisteme aktarılması üzerinde çalıştım. Excel sütunlarının okunması, hatalı kayıtların gösterilmesi, tekrar eden kayıtların engellenmesi ve adres bilgilerinden koordinat bulunması için gerekli altyapıyı hazırladım. Ardından Leaflet ve OpenStreetMap kullanarak pazarların harita üzerinde görüntülenmesini sağladım.

Veteriner taleplerinin oluşturulması, durumlarının takip edilmesi ve uygun veterinerlere yönlendirilmesi süreçlerini geliştirdim. Ayrıca ileride gerçek GPS cihazlarıyla entegre edilebilmesi amacıyla servis tabanlı ve değiştirilebilir bir GPS altyapısı hazırladım. Şimdilik örnek konum, pil seviyesi ve sinyal bilgileri üreten mock GPS sağlayıcısını kullandım.

Arayüz tarafında navbar geçişlerini, hover animasyonlarını, mobil uyumluluğu ve panel menülerini iyileştirdim. Bildirim sistemini aktif hale getirerek kullanıcıların bildirimlerini görüntüleyebilmesini ve okundu olarak işaretleyebilmesini sağladım. Profil menüsüne hesap işlemleri ekleyerek profil sayfasına geçiş, ana sayfaya dönüş ve güvenli çıkış özelliklerini tamamladım.

Çalışmalarımın sonunda projeyi test, lint, TypeScript ve production build kontrollerinden geçirerek hataları kontrol ettim. `.gitignore` dosyasını düzenleyerek gizli ortam değişkenlerinin GitHub'a yüklenmesini engelledim. Son olarak projeyi Git ile sürüm kontrolüne alıp GitHub reposuna gönderdim.
