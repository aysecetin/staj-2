
# 🌞 27 Temmuz 2026 Pazartesi
# Django Ürün, Galeri ve Kategori Yönetiminin Geliştirilmesi

## Yapılan Çalışmanın Amacı

Bugün yaptığım çalışmalarda, Django ile geliştirdiğim kurumsal tedarik sitesinin ürün, galeri ve kategori yönetimini daha işlevsel ve sürdürülebilir hâle getirdim. Galeri görsellerinin ürünlerde tekrar kullanılabilmesini sağlayarak gereksiz dosya tekrarını önledim, ürünlerin kategori bazlı daha düzenli yönetilmesini sağladım ve görselleri hem kullanıcı deneyimi hem de performans açısından optimize ettim. Ayrıca canlı sunucuya güncellemeleri güvenli şekilde aktararak sistemin sorunsuz çalıştığını doğruladım.

---

## Galeri Görsellerinin Düzenlenmesi

- Galeri sayfasındaki ürün fotoğraflarının kart çerçevelerine tam olarak oturmadığını tespit ettim.
- Görsellerde kullanılan `object-fit: cover` özelliğinin fotoğrafları üstten, alttan veya yanlardan kırptığını belirledim.
- Ürünlerin tamamının görünmesi için galeri görsellerinde `object-fit: contain` özelliğini kullandım.
- Galeri kartlarının **4:3** görüntü oranını korudum.
- Farklı boyutlardaki fotoğrafların eşit büyüklükteki kartlarda gösterilmesini sağladım.
- Görseller ile kart arasında oluşabilecek boş alanlara açık krem renkli arka plan ekledim.
- Görselleri kartların yatay ve dikey merkezine hizaladım.
- Galeri fotoğraflarına `loading="lazy"` özelliği ekleyerek sayfa açılış performansını artırdım.
- Tarayıcı önbelleğinin eski CSS dosyasını kullanmaması için statik dosya sürüm bilgisini güncelledim.

---

## Ürün Fotoğraflarının Arka Planlarının Düzenlenmesi

- Ürün fotoğraflarındaki gereksiz arka planları kaldırdım.
- Kavanoz, paket ve ambalaj bölümlerini koruyarak yalnızca arka plan alanlarını temizledim.
- Kenarlarda oluşabilecek bozuklukları ve renk kalıntılarını kontrol ettim.
- Arka planı kaldırılan görselleri kart içerisinde daha dikkat çekici olacak şekilde düzenledim.
- Tüm ürün fotoğraflarını benzer görsel standartlara ulaştırdım.
- Galeri ve ürün kartlarında daha profesyonel bir görünüm elde ettim.
- Küçük ekranlarda ve farklı kart boyutlarında görsellerin okunabilirliğini test ettim.

---

## Galeri ve Ürünler Arasında Bağlantı Kurulması

- Galeri görselleri ile ürün kayıtlarının birbirinden bağımsız olduğunu tespit ettim.
- Aynı fotoğrafın tekrar yüklenmesini önlemek amacıyla ürün modeli ile galeri modeli arasında ilişki kurdum.
- `ProductService` modeline `gallery_image` isimli yeni alan ekledim.
- Bu alanı `GalleryImage` modeliyle `ForeignKey` ilişkisi kuracak şekilde yapılandırdım.
- Yönetim panelinde ürün eklerken daha önce yüklenmiş galeri görsellerinin seçilebilmesini sağladım.
- Galeri görseli silindiğinde ürün kaydının korunması için `on_delete=models.SET_NULL` kullandım.
- Galeri görseli seçimini zorunlu tutmayarak mevcut kayıtların bozulmasını engelledim.
- Eski ürünlerde doğrudan yüklenen görsellerin çalışmaya devam etmesini sağladım.
- `display_image` özelliğini oluşturarak varsa galeri görselinin, yoksa eski ürün görselinin kullanılmasını sağladım.

---

## Kategori İçerisinden Ürün Yönetiminin Geliştirilmesi

- Django yönetim panelindeki kategori düzenleme ekranını geliştirdim.
- Her kategori sayfasına ilgili ürünlerin listelendiği **inline** yönetim alanı ekledim.
- Yönetici kullanıcının kategori ekranından ayrılmadan ürün ekleyebilmesini sağladım.
- Aynı ekrandan ürün adı, açıklama, galeri görseli, öne çıkan durumu, yayın durumu ve sıralama bilgilerinin düzenlenebilmesini sağladım.
- Galeri görsellerinin aranarak seçilebilmesi için otomatik tamamlama (**autocomplete**) özelliğini kullandım.
- Mevcut ürünlerin aynı ekran üzerinden düzenlenmesini sağladım.
- Ürün detay sayfasına hızlı geçiş için değişiklik bağlantıları ekledim.

---

## Ürünler ve Hizmetler Sayfasının Güncellenmesi

- Ürün kartı şablonunu yeni galeri görseli yapısına uygun hâle getirdim.
- Doğrudan `product.image` yerine `product.display_image` yapısını kullandım.
- Galeriden seçilen görsellerin otomatik olarak ürün kartlarında gösterilmesini sağladım.
- Yayında olmayan ürünlerin listeleme sorgularından çıkarılmasını sağladım.
- Ürün kartlarında da `object-fit: contain` kullanarak görsellerin kırpılmasını engelledim.
- Ürünleri kategori başlıkları altında düzenli şekilde listeledim.
- Ana sayfadaki öne çıkan ürünlerde de galeri görsellerinin kullanılmasını sağladım.
- Veritabanı sorgularını azaltmak amacıyla `select_related` ve `Prefetch` kullandım.

---

## Veritabanı ve Test İşlemleri

- `0006_productservice_gallery_image.py` migration dosyasını oluşturdum.
- Galeri görselinin ürün kaydında doğru kullanılmasını doğrulayan otomatik test yazdım.
- Ürünler sayfasında doğru görsel URL'sinin gösterildiğini test ettim.
- Toplam iki otomatik testi çalıştırarak başarıyla tamamlandığını doğruladım.
- `python manage.py check` komutuyla sistem kontrolünü gerçekleştirerek herhangi bir yapılandırma hatası olmadığını doğruladım.

---

## GitHub ve Canlı Sunucu İşlemleri

- Yaptığım değişiklikleri Git ile versiyon kontrolüne ekledim.
- Galeri–ürün entegrasyonunu açıklayan commit oluşturdum.
- Commit'i GitHub üzerindeki `main` branch'ine gönderdim.
- Canlı sunucuya bağlanarak `git pull` ile güncel kodları aktardım.
- Migration işleminden önce SQLite veritabanının yedeğini aldım.
- Yeni migration dosyasını canlı ortamda uyguladım.
- Güncellenen CSS dosyalarının kullanılabilmesi için `collectstatic` komutunu çalıştırdım.
- Gunicorn servisini kesintisiz şekilde yeniden yükledim.
- HTTPS yönlendirmesini ve canlı sistemin sorunsuz çalıştığını kontrol ettim.

---

## Kazanımlar

- Django modelleri arasında `ForeignKey` ilişkileri kurma konusunda deneyim kazandım.
- Django Admin içerisinde **inline** ürün yönetimi geliştirmeyi öğrendim.
- Aynı görselin birden fazla bölümde tekrar yüklenmeden kullanılmasını sağladım.
- `select_related` ve `Prefetch` kullanarak sorgu optimizasyonu gerçekleştirdim.
- Responsive galeri ve ürün kartlarında `object-fit` kullanımını geliştirdim.
- Ürün fotoğraflarının arka planlarını düzenleyerek görsel standardizasyon sağladım.
- Migration, veritabanı yedekleme, otomatik test, GitHub ve canlı sunucu güncelleme süreçlerini uygulamalı olarak gerçekleştirdim.
