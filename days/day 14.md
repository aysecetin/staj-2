
# 21 Temmuz 2026 Salı

Bugün geliştirdiğim Django tabanlı web projesini canlı ortama taşımak için gerekli sunucu ve alan adı altyapısını hazırlama çalışmaları yaptım. İlk olarak proje için altinertoptan.com alan adını satın aldım ve alan adının yönetim ayarlarını inceledim. Alan adı kayıt işlemlerini tamamlayarak daha sonra kullanılacak DNS yapılandırmaları için gerekli hazırlıkları yaptım.

Canlı yayın ortamı oluşturmak amacıyla DeHost üzerinden yeni bir VPS (Virtual Private Server) kiraladım. Sunucu oluşturulduktan sonra SSH bağlantısı kurarak Ubuntu sunucusuna erişim sağladım. Sunucuda sistem paketlerini güncelledim ve CloudPanel kurulumuna başlamadan önce gerekli bağımlılıkları kontrol ettim.

CloudPanel kurulumu sırasında veritabanı servisleri ile ilgili hatalar oluştuğunu tespit ettim. Hata kayıtlarını inceleyerek problemin nedenini araştırdım ve yarım kalan paket kurulumlarını kontrol ettim. Sorunun mevcut sistem yapılandırmasından kaynaklanabileceğini değerlendirdiğim için sunucuyu tamamen sıfırlayarak Ubuntu 22.04 işletim sistemini yeniden kurdum.

İşletim sistemi yeniden kurulduktan sonra SSH erişimini tekrar test ettim. Bağlantı probleminin kendi bilgisayarımdan mı yoksa sunucu taraflı mı olduğunu anlamak amacıyla farklı ağlar üzerinden bağlantı denemeleri gerçekleştirdim. Ev interneti ve mobil internet bağlantıları üzerinden SSH ve ağ erişim testleri yaptım. Ayrıca ping ve port erişim kontrolleri gerçekleştirerek bağlantı problemini analiz ettim.

# değiştir burayı
Yapılan testler sonucunda problemin istemci bilgisayardan değil, sunucu tarafındaki ağ veya servis yapılandırmasından kaynaklandığını belirledim. Elde ettiğim test sonuçlarını ve hata çıktılarını kayıt altına alarak hosting sağlayıcısının teknik destek ekibine iletilmek üzere gerekli teknik bilgileri hazırladım. Böylece canlı yayın öncesinde sunucu altyapısındaki erişim probleminin tespit edilmesi ve giderilmesi için gerekli ön hazırlıkları tamamladım.
