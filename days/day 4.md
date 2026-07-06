## 🌞 6 Temmuz 2026 Pazartesi 


**Django, PostgreSQL ve Canlı Yayın Altyapısı**

Stajımın dördüncü gününde statik olarak hazırladığım e-ticaret sitesini Django altyapısına dönüştürdüm. Çalışan demoyu korumak amacıyla GitHub üzerinde django-gecis isimli ayrı bir geliştirme dalı oluşturdum.
  
Django projesini modüler bir yapıda hazırladım. Ürün ve kategori işlemleri için catalog, sipariş işlemleri için orders, genel site ayarları için core uygulamalarını oluşturdum. Ürün, kategori, sipariş, sipariş kalemi, durum geçmişi ve bildirim kaydı modellerini hazırladım. Veritabanı geçişlerini uyguladım ve örnek ürünleri sisteme ekledim.
  
Django yönetim panelini yapılandırarak ürünlerin, kategorilerin, siparişlerin ve sipariş durumlarının yönetilebilmesini sağladım. Canlı ve yerel ortamlar için ayrı admin hesapları oluşturdum. Müşteri tarafından oluşturulan siparişlerin PostgreSQL veritabanına kaydedilmesini ve admin panelinde görüntülenmesini sağladım.
  
Sipariş kodunun otomatik oluşturulması, sipariş takibi ve fiyatların güvenli biçimde sunucu tarafından hesaplanması özelliklerini geliştirdim. Sistemin çalışmasını doğrulamak için otomatik testler yazdım. Ürün API’si, sipariş oluşturma, sipariş takibi, e-posta bildirimi ve istemci tarafından gönderilen sahte fiyatların dikkate alınmaması gibi durumları test ettim.
  
Projeyi Render platformunda yayımladım. Render üzerinde Django web servisi ve PostgreSQL veritabanı oluşturdum. GitHub’daki django-gecis dalına gönderilen değişikliklerin otomatik olarak yayımlanmasını sağladım.
  
Yeni sipariş oluştuğunda satıcıya e-posta gönderilmesi için bildirim sistemi geliştirdim. Render’ın ücretsiz paketinde Gmail SMTP bağlantılarının engellendiğini tespit ettim. Bu nedenle sistemi HTTPS üzerinden çalışan Resend API’ye uyarladım. Canlı ortamda test siparişleri oluşturarak siparişlerin PostgreSQL’e kaydedildiğini, admin panelinde görüntülendiğini ve bildirim sonuçlarının kayıt altına alındığını doğruladım.
  
Son olarak projenin uzun vadeli barındırma seçeneklerini araştırdım. Render, DeHost, Turkishost ve VPS/VDS çözümlerini maliyet, yedekleme, performans, güvenlik ve birden fazla site barındırma açısından karşılaştırdım. Birden fazla firma sitesi için Docker, Nginx ve PostgreSQL kullanılan ortak bir VPS altyapısının daha ekonomik olabileceğini değerlendirdim.
