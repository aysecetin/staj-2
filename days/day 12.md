# 🌞 17 Temmuz 2026 Cuma


Bugün SürüTakip platformunun mevcut Next.js yapısını Django altyapısına taşıdım. Geçiş süreci boyunca mevcut tasarımın ve kullanıcı deneyiminin korunmasına özen gösterdim. Tüm geliştirmeleri `django-migration` isimli ayrı bir Git dalı üzerinde gerçekleştirdim.

Kullanıcı, veteriner ve yönetici panellerindeki sayfaları Django şablon sistemine uyarladım. Kullanıcı panelinde hayvan, ürün, ilan, veteriner talebi, abonelik ve profil işlemlerini düzenledim. Eksik olan ilan oluşturma ve kayıt yönetimi özelliklerini geliştirerek sisteme ekledim.

GPS takip bölümünü Leaflet ve OpenStreetMap kullanarak yeniden düzenledim. Hayvanların güncel konumlarının harita üzerinde görüntülenmesini sağladım. Harita üzerindeki işaretçilere cihaz bilgileri ile **"Cihaz ayrıntılarını gör"** bağlantısını ekledim. Cihaz detay sayfasında pil seviyesi, sinyal gücü, bağlı hayvan bilgisi, son konum ve konum geçmişi gibi bilgilerin görüntülenmesini sağladım.

Bildirim ve hesap menülerini yeniden düzenledim. Haritanın açılır menülerin üzerine çıkmasına neden olan katman sırası problemini CSS `z-index` değerlerini düzenleyerek çözdüm. Profilim, ana siteye git ve çıkış yap seçeneklerinin tüm sayfalarda doğru şekilde görüntülenmesini sağladım.

Veteriner profil sayfasını geliştirdim. Veterinerlerin ad-soyad, telefon, diploma numarası, uzmanlık alanı, çalışma bölgesi, klinik bilgileri, adres, açıklama ve profil fotoğrafı gibi bilgilerini güncelleyebileceği alanları oluşturdum. Ayrıca profil doluluk oranını ve veteriner onay durumunu gösteren bölümleri ekledim.

Yönetim panelindeki **Hayvan Pazarları** bölümüne Excel'den veri yükleme özelliğini geliştirdim. `.xlsx` dosyalarından pazar adı, il, ilçe, adres, koordinatlar, pazar günü ve yetkili kurum bilgilerinin okunmasını sağladım. Mevcut kayıtların güncellenmesi, yeni kayıtların eklenmesi ve hatalı satırların kullanıcıya bildirilmesi işlemlerini gerçekleştirdim. Bunun yanında dosya boyutu kontrolü ve koordinat doğrulama mekanizmalarını da sisteme ekledim.

Yaptığım geliştirmelerin ardından Django sistem kontrollerini ve otomatik testleri çalıştırdım. Toplam **12 adet testin** başarıyla tamamlandığını doğruladım ve sistemde herhangi bir yapılandırma hatası bulunmadığını kontrol ettim.
