# 🌞 13 Temmuz 2026 Pazartesi 

Bugün OtoParça Bul projesinde kullanıcı güvenliği, yönetim akışı ve arayüz kullanılabilirliği üzerine geliştirmeler yaptım. Öncelikle parçacı paneli ve müşteri tarafındaki sayfaları inceleyerek hangi alanların kullanıcı deneyimini karmaşıklaştırdığını belirledim.

Navbar yapısını sadeleştirdim. Daha önce üst menüde yer alan Parçacı Profili ve Parçacı Paneli bağlantılarını kaldırarak GitHub benzeri bir profil menüsü oluşturdum. Sağ üstte parçacı hesabını temsil eden sade bir avatar alanı bıraktım. Bu avatara tıklandığında Genel Bakış, Stoklarım, Mal Kabul, Stok Partileri, Perakende Satış, Satış Geçmişi, Stok Hareketleri, Depolarım, Cari Hesaplar, Gelen Talepler, Dükkan Profilim ve Paketim bağlantılarının açılmasını sağladım.

Arayüzdeki boşlukları azaltarak sayfaların daha dengeli ve ortalı görünmesini sağladım. Header, footer, ana sayfa ve panel yapılarında genişlik ayarlarını düzenledim. Böylece özellikle geniş ekranlarda içeriklerin ortada sıkışmış gibi görünmesini engelledim.

Dark mode tarafında okunabilirlik sorunlarını giderdim. Bazı rozet, buton ve kart yazılarının koyu temada yeterince okunmadığını fark ettim. Dark mode için arka plan, kart, border, metin, rozet ve buton renklerini yeniden düzenledim. Özellikle “Stokta var”, “Pilot parçacı” ve benzeri etiketlerin koyu temada daha net görünmesini sağladım.

Parçacı katılım formunu çalışır hale getirdim. Daha önce formdaki “Demo başvuru gönder” butonu sadece görsel olarak duruyordu. Form alanlarını çalışacak şekilde düzenledim ve dükkan adı, yetkili kişi, telefon ve şehir/ilçe alanlarını zorunlu yaptım. Form gönderildiğinde başvurunun tarayıcıda demo veri olarak saklanmasını ve kullanıcıya “Demo başvuru alındı” mesajı gösterilmesini sağladım.

Admin Demo ekranını parçacı başvuru süreciyle ilişkilendirdim. Katılım formundan gönderilen başvuruların Admin Demo sayfasında “Onay bekleyen parçacılar” alanında görünmesini sağladım. Admin tarafında “Onayla” butonuna basıldığında başvurunun durumunu “Onaylandı” olarak güncelledim ve onaylanan başvurunun pilot parçacılar listesinde görünmesini sağladım. Ayrıca toplam parçacı ve onay bekleyen parçacı sayaçlarını bu yeni akışa göre güncelledim.

Güvenilir site mantığı için onaylı olmayan parçacıların müşteri tarafında görünmesini engelledim. Onaylı olmayan bir parçacının ürünlerinin parça arama sonuçlarında listelenmemesini sağladım. Ayrıca onaysız bir parçanın detay sayfasına doğrudan linkle gidilirse “Bu parça yayında değil” mesajı gösterilecek şekilde kontrol ekledim. Benzer parçalar alanında da yalnızca onaylı parçacıların ürünlerinin görünmesini sağladım.

Parçacı profil sayfasında da güvenlik kontrolü ekledim. Onaylı olmayan bir dükkanın profiline doğrudan gidildiğinde, kullanıcının ürünleri ve dükkan bilgilerini görmesi yerine “Bu dükkan henüz onay sürecinde” mesajı gösterilecek şekilde düzenleme yaptım.

Bu geliştirmeler sonucunda OtoParça Bul projesinde parçacı başvuru, admin onayı ve müşteri tarafında güvenilir listeleme akışı daha gerçekçi hale geldi. Artık sisteme başvuran her parçacı doğrudan yayına alınmıyor; önce admin onayından geçiyor. Böylece platformun güvenilirlik mantığı prototip üzerinde daha net şekilde gösterilmiş oldu.
