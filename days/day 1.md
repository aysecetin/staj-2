## 1 Temmuz 2026

**01.07.2026 – Analiz ve Proje Planlama Toplantısı**

Bugün yaklaşık iki saat süren proje planlama ve analiz toplantısına katıldım. Toplantıda, sanayi işletmelerinin dijitalleşme süreçlerinde karşılaştıkları problemler değerlendirildi ve geliştirilecek web tabanlı stok ve işletme yönetim sistemi için ihtiyaç analizi yapıldı.
  
İlk olarak hedef kullanıcı kitlesi ve mevcut çalışma yöntemleri incelendi. Özellikle küçük ve orta ölçekli işletmelerin stok takibini çoğunlukla manuel yöntemlerle veya yetersiz yazılımlarla yürüttüğü, işletme büyüdükçe daha kapsamlı yönetim sistemlerine ihtiyaç duyduğu üzerine değerlendirmeler yapıldı. Geliştirilecek sistemin bu ihtiyaçları karşılayacak şekilde modüler bir yapıda tasarlanmasının uygun olacağı kararlaştırıldı.
  
Toplantıda temel modüller üzerinde fikir alışverişi yapıldı. İlk aşamada stok yönetimi, depo yönetimi ve cari hesap işlemlerinin geliştirilmesi planlandı. Daha sonraki sürümlerde faturalandırma ve ek finansal modüllerin sisteme dahil edilmesi üzerine değerlendirmeler gerçekleştirildi. Modüllerin birbirinden bağımsız geliştirilebilmesi ve ilerleyen süreçte sisteme yeni özelliklerin kolayca eklenebilmesi için ölçeklenebilir bir mimari oluşturulmasının öneminden bahsedildi.

Veritabanı tasarımı hakkında ön değerlendirmeler yapıldı. PostgreSQL kullanılması planlanan sistemde ürün, işletme, kullanıcı, depo ve stok hareketleri gibi temel tabloların oluşturulması gerektiği konuşuldu. Ürün görsellerinin doğrudan veritabanında tutulması yerine URL üzerinden yönetilmesinin performans açısından daha uygun olacağı değerlendirildi.

Kullanıcı yönetimi tarafında farklı yetki seviyelerine sahip hesapların bulunması gerektiği üzerinde duruldu. İşletme yöneticileri ve çalışanların farklı erişim yetkilerine sahip olması, işletme profili ile kullanıcı profillerinin birbirinden ayrılması ve çoklu kullanıcı desteğinin sağlanması gibi konular ele alındı.

Ürün yönetimi kısmında ürün durumlarının takip edilebilmesi, alış ve satış bilgilerinin kayıt altına alınması, farklı para birimlerinin desteklenmesi ve temel kârlılık analizlerinin yapılabilmesi üzerine fikir alışverişinde bulunuldu. Ayrıca işletmelerin birden fazla depo kullanabilmesi ve stok hareketlerinin detaylı şekilde izlenebilmesi gerektiği değerlendirildi.

Sistemin kullanıcı deneyimini artıracak bazı özellikler de toplantıda gündeme geldi. Ürün arama süreçlerinin geliştirilmesi, harita üzerinden işletmelerin görüntülenebilmesi, ürün taleplerinin oluşturulabilmesi, favori ürünler ve bildirim sistemi gibi fonksiyonların ilerleyen sürümlerde eklenebileceği konuşuldu. Bunun yanında yapay zekâ destekli bazı özelliklerin (görsel veya ses ile arama, analiz desteği vb.) gelecekte projeye değer katabilecek geliştirmeler arasında yer alabileceği değerlendirildi.

Toplantının son bölümünde sistemin web tabanlı olarak geliştirilmesi ve Python teknolojileri kullanılarak ilerlenmesi üzerine planlama yapıldı. Projenin aşamalı olarak geliştirilmesi, öncelikle temel modüllerin tamamlanması ve ihtiyaçlar doğrultusunda yeni özelliklerin sonraki sürümlerde sisteme eklenmesi yönünde bir yol haritası oluşturuldu. Ayrıca yazılımın ölçeklenebilir ve sürdürülebilir bir yapıda tasarlanmasının, ilerleyen süreçte yapılacak geliştirmeleri kolaylaştıracağı değerlendirildi.

Bu toplantı sayesinde bir yazılım projesinin geliştirme aşamasına geçmeden önce gerçekleştirilen ihtiyaç analizi, sistem tasarımı ve modül planlamasının proje başarısı açısından ne kadar önemli olduğu konusunda önemli bilgiler edinmiş oldum.
