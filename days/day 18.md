
# 🌞 27 Temmuz 2026 Pazartesi

Django Ürün, Galeri ve Kategori Yönetiminin Geliştirilmesi
Yapılan Çalışmanın Amacı
Dün akşam yaptığım çalışmalarda, Django ile geliştirdiğim kurumsal tedarik sitesinin galeri ve ürün yönetimini daha kullanışlı hâle getirdim. Yönetim panelinden eklenen ürünlerin kategorilere ayrılmasını, galeri görsellerinin ürünlerde tekrar kullanılmasını ve ürünlerin site üzerinde daha düzenli sergilenmesini sağladım. Ayrıca ürün fotoğraflarının arka planlarını kaldırarak daha temiz ve profesyonel bir görünüm elde ettim.
Galeri Görsellerinin Düzenlenmesi
Galeri sayfasındaki ürün fotoğraflarının kart çerçevelerine tam olarak oturmadığını tespit ettim.

Görsellerde kullanılan object-fit: cover özelliğinin fotoğrafları çerçeveyi doldurmak için üstten, alttan veya yanlardan kırptığını belirledim.

Ürünlerin tamamının görünmesi için galeri görsellerinde object-fit: contain özelliğini kullandım.

Galeri kartlarının 4:3 görüntü oranını korudum ve farklı boyutlardaki fotoğrafların eşit büyüklükteki kartlarda gösterilmesini sağladım.

Görsel ile kart arasında oluşabilecek boş alanlara açık krem renkli bir arka plan ekledim.

Görselleri kartların yatay ve dikey merkezine hizaladım.

Galeri fotoğraflarına loading="lazy" özelliği ekledim. Böylece kullanıcı sayfayı açtığında ekranda görünmeyen görsellerin daha sonra yüklenmesini ve sayfanın daha hızlı açılmasını sağladım.

Tarayıcının eski CSS dosyasını önbellekten göstermemesi için statik dosya sürüm bilgisini güncelledim.

Ürün Fotoğraflarının Arka Planlarının Kaldırılması
Ürün fotoğraflarındaki gereksiz ve görüntü bütünlüğünü bozan arka planları kaldırdım.

Ürünlerin kavanoz, paket veya ambalaj bölümlerini koruyarak yalnızca arka plan alanlarını temizledim.

Fotoğrafların kenarlarında oluşabilecek bozuklukları ve istenmeyen renk kalıntılarını kontrol ettim.

Arka planı kaldırılan ürünleri kart içerisinde daha net ve dikkat çekici görünecek şekilde düzenledim.

Farklı ürün fotoğraflarının benzer görsel standartlara sahip olmasını sağladım.

Arka planı temizlenen görseller sayesinde ürünlerin galeri ve ürün kartlarında daha profesyonel görünmesini sağladım.

Görsellerin küçük ekranlarda ve farklı kart boyutlarında okunabilirliğini kontrol ettim.

Galeri ve Ürünler Arasında Bağlantı Kurulması
Mevcut sistemde galeri görselleri ile ürün kayıtlarının birbirinden bağımsız olduğunu tespit ettim.

Aynı fotoğrafın hem galeriye hem de ürünler bölümüne yeniden yüklenmesini önlemek için ürün modeli ile galeri görseli arasında ilişki kurdum.

ProductService modeline gallery_image isimli yeni bir alan ekledim.

Bu alanı Django ForeignKey yapısıyla GalleryImage modeline bağladım.

Ürün eklerken yönetim panelinden daha önce galeriye yüklenen bir görselin seçilebilmesini sağladım.

Bir galeri görseli silindiğinde bağlı ürünün tamamen silinmemesi için on_delete=models.SET_NULL seçeneğini kullandım.

Galeri görseli seçilmesini zorunlu tutmayarak mevcut ürün kayıtlarının bozulmasını engelledim.

Eski ürünlerde doğrudan yüklenen görsellerin çalışmaya devam etmesini sağladım.

Ürün için galeri görseli seçilmişse öncelikle bu görselin kullanılmasını, seçilmemişse eski ürün görselinin gösterilmesini sağlayan display_image özelliğini hazırladım.

Kategori İçerisinden Ürün Ekleme
Django yönetim panelindeki kategori düzenleme ekranını geliştirdim.

Her kategori sayfasına o kategoriye bağlı ürünlerin listelendiği bir inline alan ekledim.

Yönetici kullanıcının kategori ekranından ayrılmadan ürün ekleyebilmesini sağladım.

Kategori içerisinden aşağıdaki ürün bilgilerinin girilebilmesini sağladım:
Ürün veya hizmet adı
Ürün açıklaması
Galeri görseli
Öne çıkan durumu
Yayında durumu
Sıralama değeri

Galeri görsellerinin yönetim panelinde aranarak seçilebilmesi için otomatik tamamlama özelliğini kullandım.

Kategoriye bağlı mevcut ürünlerin aynı ekran üzerinden düzenlenebilmesini sağladım.

Detaylı ürün düzenleme sayfasına geçiş yapılabilmesi için ürün satırlarına değişiklik bağlantısı ekledim.

Ürünler ve Hizmetler Sayfasının Güncellenmesi
Ürün kartı şablonunu yeni galeri görseli yapısına uygun hâle getirdim.

Ürün kartlarında doğrudan product.image kullanmak yerine product.display_image özelliğini kullandım.

Galeriden seçilen görsellerin Ürünler / Hizmetler sayfasında otomatik olarak gösterilmesini sağladım.

Yayında olmayan ürünlerin sorgu aşamasında filtrelenmesini sağladım.

Ürün görsellerinde kırpılmayı önlemek için ürün kartlarını da object-fit: contain yapısına geçirdim.

Ürünlerin kategori başlıklarının altında sıralı ve düzenli şekilde gösterilmesini sağladım.

Ana sayfada öne çıkan ürünlerin de galeri görsellerini kullanabilmesini sağladım.

Veritabanı sorgularını azaltmak için select_related ve Prefetch kullandım.

Veritabanı ve Test İşlemleri
Modelde yaptığım değişiklik için 0006_productservice_gallery_image.py isimli migration dosyasını oluşturdum.

Galeri görselinin ürün kaydında doğru şekilde kullanılmasını kontrol eden otomatik test yazdım.

Seçilen galeri görselinin Ürünler / Hizmetler sayfasında doğru URL ile gösterilmesini test ettim.

Toplam iki otomatik testi çalıştırdım ve testlerin başarıyla tamamlandığını doğruladım.

python manage.py check komutuyla Django sistem kontrolünü çalıştırdım ve herhangi bir yapılandırma hatası olmadığını gördüm.

GitHub ve Canlı Sunucu İşlemleri
Yaptığım değişiklikleri Git ile takip altına aldım.

Galeri–ürün entegrasyonu için açıklayıcı bir commit oluşturdum.

Commiti GitHub üzerindeki projenin main branch’ine gönderdim.

Canlı sunucuya bağlanarak güncel kodları git pull komutuyla çektim.

Migration işleminden önce SQLite veritabanının yedeğini aldım.

Yeni veritabanı alanını canlı sisteme eklemek için migration işlemini uyguladım.

Statik CSS dosyalarını canlı ortamda güncellemek için collectstatic komutunu çalıştırdım.

Gunicorn servisindeki çalışan uygulamayı kesintiye uğratmadan yeniden yükledim.

Uygulamanın HTTPS yönlendirmesini ve canlı sunucunun yanıt verdiğini kontrol ettim.

Kazanımlar
Django modelleri arasında ForeignKey ilişkisi kurma konusunda deneyim kazandım.

Django Admin içerisinde inline ürün yönetimi hazırlamayı öğrendim.

Aynı görselin birden fazla bölümde tekrar yüklenmeden kullanılmasını sağladım.

select_related ve Prefetch kullanarak sorgu optimizasyonu yaptım.

Responsive ürün ve galeri kartlarında object-fit kullanımını geliştirdim.

Ürün fotoğraflarının arka planlarını temizleyerek görsel standardizasyon çalışması yaptım.

Migration, veritabanı yedekleme, otomatik test, GitHub ve canlı sunucu güncelleme süreçlerini uygulamalı olarak gerçekleştirdim.
