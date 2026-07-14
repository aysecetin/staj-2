# 🌞 14 Temmuz 2026 Salı 


Bugün OtoParça Bul projesinde kullanıcı girişi, navbar düzeni ve panel erişim kuralları üzerinde çalıştım. Öncelikle üst menüdeki karışıklığı azaltmak için aynı sayfaya yönlenen bağlantıları sadeleştirdim. Misafir kullanıcı, giriş yapan parçacı ve admin kullanıcı için farklı menü davranışları oluşturdum.

Parçacı hesabıyla giriş yapıldığında navbar üzerinde yalnızca sık kullanılan bağlantıların görünmesini sağladım. Daha detaylı panel bağlantılarını ise profil avatarına tıklanınca açılan menü içerisine yerleştirdim. Bu menüde genel bakış, stoklar, yeni parça ekleme, mal kabul, stok partileri, perakende satış, satış geçmişi, stok hareketleri, depolar, cari hesaplar, gelen talepler ve dükkan profili gibi alanların listelenmesini sağladım. Çıkış yap butonunu da bu profil menüsünün en altına taşıdım.

Giriş yapmamış kullanıcılar için Katıl, Giriş Yap ve Parçacı Katılım butonlarının görünmesini; giriş yapan kullanıcılar için ise bu alanların gizlenmesini sağladım. Böylece kullanıcı oturumuna göre değişen daha gerçekçi bir navbar yapısı oluşturdum.

Admin Demo bağlantısını kullanıcıya açık alanlardan kaldırdım. Admin paneline erişimi ayrı bir /admin rotası üzerinden korumalı hale getirdim. Giriş yapmamış kullanıcı admin paneline gitmeye çalıştığında admin giriş ekranına yönlendirilecek şekilde düzenleme yaptım. Admin olmayan kullanıcıların URL’yi elle yazarak admin paneline erişmesini engelledim.

Parçacı paneli tarafında da güvenlik ve kullanıcı deneyimi açısından düzenleme yaptım. Çıkış yapıldıktan sonra parçacı panelinin görünmeye devam etmemesi için panel sayfalarını parçacı oturumu kontrolüne bağladım. Böylece kullanıcı çıkış yaptıktan sonra /panel adresinde kalsa bile panel içeriği gösterilmiyor ve giriş ekranına yönlendiriliyor.

Ayrıca giriş sayfasının görünümünü düzenledim. Sayfanın boş görünmesini engellemek için daha açıklayıcı bir giriş alanı oluşturdum. Giriş ekranında demo oturum mantığını anlatan metinler ve parçacı hesabıyla giriş butonu yer aldı. Sayfa yapısında footer’ın ekran ortasında kalmaması için genel layout düzenini iyileştirdim.

Bu çalışmaların sonunda OtoParça Bul projesinde kullanıcı rolüne göre değişen navbar yapısı, korumalı admin erişimi, parçacı paneli erişim kontrolü ve daha düzenli bir giriş sayfası oluşturmuş oldum. Böylece prototip, gerçek bir web uygulamasındaki oturum ve yetki akışına daha yakın hale geldi.



<img width="1461" height="839" alt="Ekran Resmi 2026-07-14 15 10 17" src="https://github.com/user-attachments/assets/0ce28eff-9212-458c-8882-16e3f751bcb8" />

<img width="1460" height="839" alt="Ekran Resmi 2026-07-14 15 10 02" src="https://github.com/user-attachments/assets/30023baf-0ea2-42f4-a218-447e9e626319" />

<img width="1469" height="889" alt="Ekran Resmi 2026-07-14 15 07 48" src="https://github.com/user-attachments/assets/1313e0b5-6b37-44d0-adef-366b5a80bc7e" />
