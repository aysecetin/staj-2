## 2 Temmuz 2026

Bugün “OtoParça Bul” isimli MVP/prototip web uygulamasını geliştirmeye başladım. Projenin amacını, oto sanayide yedek parça satan küçük işletmeler ile parça arayan müşterileri dijital ortamda buluşturmak olarak belirledim. Bu sistemde müşterilerin aradıkları parçayı web sitesi üzerinden filtreleyerek bulabilmesini, parçacıların da kendi işletmelerini dijital vitrin olarak sergileyebilmesini hedefledim.  
  
İlk olarak proje için React, Vite ve TypeScript tabanlı bir yapı kurdum. Arayüz geliştirme tarafında Tailwind CSS kullandım. Projede backend veya gerçek veritabanı kurmadım; demo amaçlı tüm verileri mock data olarak hazırladım. Böylece prototipi hızlı şekilde gezilebilir ve gösterilebilir hale getirdim.  
  
Uygulama için genel sayfa yapısını oluşturdum. React Router kullanarak sayfalar arasında geçiş sağladım. Header ve footer bileşenlerini ekledim. Mobil uyumlu menü yapısı oluşturdum. Bu sayede uygulamanın hem masaüstü hem de mobil ekranlarda kullanılabilir olmasını sağladım.
  
Ana sayfada projenin temel fikrini anlatan bir hero alanı tasarladım. Bu alanda “Aradığın oto parçasını sanayide hızlıca bul” başlığını, açıklama metnini, parça arama kutusunu ve iki ana butonu ekledim. Bu butonlardan birini müşteriyi parça arama ekranına, diğerini ise parçacı katılım formuna yönlendirecek şekilde ayarladım. Ana sayfaya ayrıca küçük parçacılara yönelik bilgilendirici bölümler, nasıl çalışır adımları, istatistik kartları ve paketler bölümü ekledim.
  
Parça arama sayfasında kullanıcıların parça adı, araç markası, model, yıl, şehir, parça türü, fiyat aralığı ve stok durumuna göre filtreleme yapabileceği bir yapı oluşturdum. Sonuç kartlarında parça adı, araç uyumluluğu, parça türü, fiyat, stok durumu, parçacı adı, konum bilgisi, WhatsApp ile sor butonu ve detayları gör butonunu gösterdim.
  
Parça detay sayfasında seçilen parçaya ait detaylı bilgileri listeledim. Bu sayfada parça adı, marka/model/yıl bilgisi, OEM kodu, parça türü, stok adedi, fiyat, açıklama, satıcı bilgisi, konum, telefon ve WhatsApp butonu yer aldı. Ayrıca “Parçayı ayırt” butonu ve benzer parçalar alanı ekledim.
  
Parçacı profil sayfasını oluşturdum. Bu sayfayı, web sitesi olmayan küçük işletmeler için dijital vitrin mantığında tasarladım. Sayfada dükkan adı, avatar/logo alanı, açıklama, uzman olduğu markalar, konum, çalışma saatleri, telefon/WhatsApp bilgisi, öne çıkan parçalar ve güven rozetlerine yer verdim.
  
Parçacı paneli için ayrı bir dashboard yapısı geliştirdim. Sol menüde genel bakış, stoklarım, yeni parça ekle, gelen talepler, dükkan profilim ve paketim gibi bölümler oluşturdum. Dashboard ekranında toplam ürün sayısı, webde görünen ürün sayısı, gelen talep sayısı, WhatsApp tıklamaları ve düşük stoklu ürünler gibi kartlar gösterdim.
  
Stoklarım sayfasında parçacıların ürünlerini tablo şeklinde görebileceği bir ekran hazırladım. Bu tabloda parça adı, araç uyumu, stok adedi, fiyat, webde görünsün/görünmesin seçeneği, durum ve düzenle butonuna yer verdim. Ayrıca yeni ürün ekleme modalı geliştirdim. Eklenen ürünü gerçek veritabanına değil, local state içerisine ekleyerek demo amaçlı çalıştırdım. 
  
Gelen talepler sayfasında müşterilerden gelen parça taleplerini gösteren kartlar oluşturdum. Bu kartlarda müşteri adı, telefon, araç bilgisi, aranan parça, not, talep tarihi, durum bilgisi ve WhatsApp’tan dönüş butonu yer aldı. 
  
Parçacı olarak katıl sayfasında küçük işletmeleri sisteme dahil etmeye yönelik bir başvuru formu geliştirdim. Formda dükkan adı, yetkili kişi, telefon, şehir/ilçe, çalışılan parça grupları, yazılım kullanma durumu ve webde stok gösterme tercihi gibi alanlar kullandım.
  
Admin demo sayfası oluşturdum. Bu sayfada toplam parçacı, toplam parça, toplam müşteri talebi, en çok aranan parçalar, pilot parçacılar listesi ve onay bekleyen parçacılar gibi bilgileri gösterdim.
  
Projenin ilk halinde sadece dijital vitrin fikri üzerinden ilerledim. Daha sonra iş modelini geliştirerek vitrin hizmetine ek olarak stok, depo ve cari hizmetlerinin de sunulabileceği modüler bir yapı oluşturdum. Bu doğrultuda paketleri yeniden düzenledim. Vitrin Paketi, Cari Takip Paketi, Stok + Depo Paketi ve Tam Yönetim Paketi seçeneklerini ekledim. Böylece parçacıların tüm sistemi almak zorunda kalmadan ihtiyaç duydukları modülü seçebileceği bir yapı tasarladım.
  
Arayüz temasında da düzenlemeler yaptım. Yeşil ağırlıklı daha güven veren bir renk paleti kullandım. Daha sonra light mode ve dark mode desteği ekledim. Kullanıcının header üzerinden tema değiştirebilmesini sağladım. Seçilen temayı tarayıcıda saklayarak sayfa yenilendiğinde korunmasını sağladım.
  
Ana sayfadaki hero alanı için görsel kullanımını geliştirdim. Önce bir sanayi/yedek parça dükkanı görseli ekledim. Daha sonra ikinci bir sanayi görselini projeye dahil ettim. Hero alanında bu iki görselin döngü halinde yumuşak geçişle değişmesini sağladım. Böylece sayfanın daha canlı ve gerçekçi görünmesini hedefledim.
  
Son olarak README dosyasını güncelledim. README içerisinde projenin amacı, kullanılan teknolojiler, modüler paket yapısı, sayfalar, kurulum adımları, GitHub’a güncelleme gönderme komutları ve demo notlarını detaylı şekilde yazdım.
  
Bugünün sonunda React, Vite, TypeScript ve Tailwind CSS kullanarak responsive, gezilebilir, mock data ile çalışan modern bir MVP prototipi geliştirdim. Projeyi GitHub’a yüklenebilir ve Vercel üzerinden canlı link olarak paylaşılabilir hale getirdim.
  
