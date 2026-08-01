
# 🌞 31 Temmuz 2026 Cuma

Patronumdan gelen geri bildirimleri inceleyerek mobil uygulamadaki ürün, hayvan, ilan ve veteriner süreçlerinde yapılması gereken düzenlemeleri belirledim.

İlan oluşturma ekranındaki açıklama alanında bulunan en az 20 karakter kullanma zorunluluğunu kaldırdım. Böylece kullanıcıların kısa açıklamalarla da ilan oluşturabilmesini sağladım.

Ürün veya hayvan eklerken bulunan “Satışa uygun” seçeneğinin çalışma şeklini geliştirdim. Bu seçenek işaretlendiğinde ilgili kayıt için otomatik olarak satış ilanı oluşturulmasını sağladım.

Otomatik oluşturulan ilanların sistemde aktif olan bütün hayvan pazarlarında doğrudan yayınlanmasını sağladım. Böylece kullanıcıların ürün veya hayvanı kaydettikten sonra ayrıca ilan oluşturup pazarları tek tek seçmesine gerek kalmadı.

Satışa uygun bir hayvan veya ürünün bilgileri değiştirildiğinde mevcut ilanının da otomatik olarak güncellenmesini sağladım. Satış seçeneği kaldırıldığında ilgili ilanı otomatik olarak pasif hale getirdim.

Daha önce satışa uygun olarak kaydedilmiş mevcut ürün ve hayvanların da yeni otomatik ilan sistemine aktarılabilmesi için bir eşitleme komutu geliştirdim. Bu komutu canlı ortamın dağıtım sürecine ekledim.

Hayvan ekleme ekranındaki tür, cins ve ırk alanlarında bulunan sınıflandırma hatasını giderdim. Önceden Büyükbaş, Küçükbaş, İnek, Dana, Koyun ve Keçi gibi farklı seviyelerdeki seçenekler aynı listede gösteriliyordu.

Hayvan sınıflandırmasını üç aşamalı ve birbirine bağlı bir yapıya dönüştürdüm. Kullanıcı artık önce Büyükbaş veya Küçükbaş grubunu, ardından bu gruba uygun hayvan cinsini ve son olarak ilgili ırkı seçebiliyor.

Büyükbaş grubu için inek, dana, boğa, düve ve manda seçeneklerini oluşturdum. Küçükbaş grubu için koyun, keçi, koç, kuzu ve oğlak seçeneklerini tanımladım.

Hayvan cinslerine uygun ırkları sisteme ekledim. Büyükbaş hayvanlar için Holstein, Simental, Montofon, Jersey ve Anadolu Mandası; küçükbaş hayvanlar için Sakız, Merinos, Akkaraman, İvesi, Kıvırcık ve Saanen gibi ırk seçeneklerini hazırladım.

Kullanıcının seçtiği hayvan grubuna göre yalnızca uygun cinslerin, seçtiği cinse göre de yalnızca uygun ırkların gösterilmesini sağlayan dinamik form yapısını geliştirdim.

Mevcut hayvan kayıtlarının yeni grup, cins ve ırk yapısına veri kaybı oluşmadan aktarılması için Django migration dosyaları hazırladım ve migration işlemlerini başarıyla uyguladım.

Hayvan kayıtlarına düzenleme bağlantısı ekledim. Böylece kullanıcıların mevcut hayvanın sınıflandırma, sağlık, fiyat ve satış durumunu sonradan değiştirebilmesini sağladım.

Veteriner kullanıcıları için ayrı bir hesap oluşturma ekranı hazırladım. Veterinerlerin ad, e-posta, telefon, diploma numarası, uzmanlık alanı, il, ilçe ve şifre bilgileriyle başvuru yapabilmesini sağladım.

Ortak giriş ekranını hem sürü yöneticilerinin hem de veterinerlerin kullanabileceği şekilde düzenledim. Giriş ekranına sürü yöneticisi ve veteriner hesabı oluşturma bağlantılarını ayrı ayrı ekledim.

Veteriner kullanıcıların kendilerine ait panele yönlendirilmesini sağladım. Güvenlik amacıyla yeni veteriner hesaplarının yönetici onayından sonra sağlık taleplerine erişebilmesini sağlayan mevcut onay mekanizmasını korudum.

Veteriner panelini geliştirerek bölgedeki hayvan sağlık taleplerinin görüntülenmesini sağladım. Veterinerlerin belirtileri, açıklamaları, aciliyet durumunu ve hayvan sahibi tarafından yüklenen fotoğrafları inceleyebilmesini sağladım.

Veterinerin sağlık talebine yanıt verebilmesi ve taleple ilgilendiğini belirtebilmesi için ayrıntılı bir değerlendirme ekranı hazırladım.

Veteriner kullanıcıların da APK üzerinden bildirim alabilmesi için mobil cihaz kayıt yetkilerini güncelledim.

Canlı ortamda veteriner panelinin kontrol edilebilmesi amacıyla onaylı bir demo veteriner hesabının otomatik oluşturulmasını sağladım.

Yaptığım değişikliklerin doğruluğunu kontrol etmek için kısa açıklama, otomatik ilan oluşturma, pazar eşleştirme, hayvan sınıflandırması ve veteriner kayıt süreçlerine yönelik yeni otomatik testler yazdım.

Projenin Django sistem kontrollerini ve migration tutarlılık kontrollerini çalıştırdım. Toplam 53 otomatik testin tamamının başarıyla geçtiğini doğruladım.

Web uygulamasında yapılan bu geliştirmelerin WebView tabanlı APK’ya yeniden APK derlemesi gerektirmeden yansıyacağı yapıyı korudum. Böylece canlı ortam güncellendiğinde kullanıcıların uygulamayı kapatıp açarak yeni özelliklere erişebilmesini sağladım.
