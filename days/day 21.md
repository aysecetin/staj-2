
# 🌞 30 Temmuz 2026 Perşembe

## SürüTakip Mobil Uygulamasının WebView Tabanlı Yapıya Dönüştürülmesi

### Yapılan Çalışmanın Amacı

Bugün, GPS destekli sürü yönetimi, hayvan kayıtları, hayvan pazarları, veteriner yönetimi ve abonelik işlemlerini içeren **SürüTakip** mobil uygulamasının mimarisini yeniden düzenledim. Patronumun talebi doğrultusunda mobil uygulamanın web uygulamasından bağımsız bir arayüze sahip olması yerine, mevcut Django tabanlı web sisteminin APK içerisinde çalıştırılmasına karar verildi. Bu sayede web tarafında yapılan güncellemelerin mobil uygulamaya da anında yansıması sağlandı.

---

## WebView Tabanlı Mobil Yapının Oluşturulması

- React Native projesine **react-native-webview** paketini ekledim.
- Expo uygulamasının ana ekranını WebView tabanlı olacak şekilde yeniden düzenledim.
- Canlıdaki **https://surutakip.onrender.com** adresinin APK içerisinde açılmasını sağladım.
- Böylece web uygulamasındaki tüm ekranların mobil uygulama içerisinde görüntülenmesini sağladım.
- Hayvan kayıtları, hayvan pazarları, GPS takip sistemi, veteriner işlemleri, kontrol paneli ve örnek "Bulut" isimli hayvan kayıtlarının mobil uygulamada da eksiksiz çalışmasını sağladım.

---

## Oturum Yönetimi

- Kullanıcının web uygulamasında yaptığı giriş işleminin mobil uygulama içerisinde de korunmasını sağladım.
- Daha önce geliştirilen ayrı mobil giriş ekranı ve yönlendirme yapısını sadeleştirdim.
- Web sistemindeki oturum bilgilerinin WebView içerisinde kullanılmasını sağlayarak tekrar giriş yapılmasını gerektirmeyen bir yapı oluşturdum.

---

## Mobil Kullanıcı Deneyimi

- Android cihazın geri tuşunu WebView geçmişiyle ilişkilendirdim.
- Kullanıcının uygulama içerisinde ziyaret ettiği sayfalar arasında geri tuşuyla dolaşabilmesini sağladım.
- Uygulama dışından açılması gereken bağlantıların cihazın varsayılan internet tarayıcısında açılmasını sağladım.
- Sayfa yüklenirken yükleme göstergesi ekledim.
- İnternet bağlantısı kurulamadığında kullanıcıya yeniden deneme seçeneği sunan hata ekranı geliştirdim.

---

## Bildirim Altyapısının Geliştirilmesi

- Expo üzerinden alınan bildirim anahtarını (Expo Push Token) canlı Django sistemine gönderen bağlantıyı geliştirdim.
- Kullanıcı bildirim izni verdiğinde cihazın ilgili kullanıcı hesabıyla eşleştirilmesini sağladım.
- Bildirim üzerinden uygulama açıldığında bildirim türüne göre ilgili sayfaya yönlendirme yapılabilmesi için gerekli altyapıyı hazırladım.
- GPS, veteriner, hayvan listesi ve kontrol paneli gibi farklı ekranlara yönlendirme senaryolarını oluşturdum.

---

## Django Tarafındaki Geliştirmeler

- Mobil cihazların sisteme kaydedilebilmesi için yeni bir API endpoint'i oluşturdum.
- Endpoint üzerinde kullanıcı oturumu doğrulaması ekledim.
- Cihaz platformu bilgisi ve Expo bildirim anahtarı doğrulamalarını gerçekleştirdim.
- Mobil cihaz bilgilerinin güvenli şekilde veritabanına kaydedilmesini sağladım.

---

## Test ve Doğrulama

- Mobil cihaz kayıt işlemi için otomatik Django testleri yazdım.
- Projede bulunan toplam **49 testin** başarıyla tamamlandığını doğruladım.
- React Native projesinde TypeScript kontrollerini çalıştırdım.
- Kod kalitesi kontrollerini tamamladım.
- Android JavaScript paketleme işlemini test ederek uygulamanın sorunsuz şekilde derlenebildiğini doğruladım.

---

## Sürüm Yönetimi ve Yayınlama

- Yaptığım değişiklikleri Git ile kaydettim.
- Değişiklikleri **feature/mobile-foundation** dalına göndererek GitHub deposunu güncelledim.
- GitHub üzerinden Render platformunda başlayan otomatik dağıtım sürecini takip ettim.
- Yeni sürümün canlı ortama başarıyla aktarıldığını doğruladım.

---

## APK Derleme Süreci

- Expo EAS Build kullanarak Android APK derlemesini başlattım.
- Ücretsiz kullanım sırası nedeniyle oluşan beklemenin sistem hatası olmadığını doğruladım.
- Derleme tamamlandıktan sonra APK dosyasını indirerek Android cihaz üzerinde kurulumunu gerçekleştirdim.
- Mobil uygulamanın sorunsuz şekilde çalıştığını test ederek doğruladım.

---

## Elde Edilen Sonuç

Bu çalışma sonucunda **SürüTakip** mobil uygulaması, web uygulamasıyla tamamen entegre çalışan WebView tabanlı bir yapıya dönüştürüldü. Böylece web tarafında yapılan içerik, tasarım ve sistem güncellemelerinin yeni APK oluşturmaya gerek kalmadan mobil uygulamada da anında görüntülenmesi sağlandı. Yalnızca uygulamanın cihaza özgü yerel özelliklerinde değişiklik yapılması gerektiğinde yeniden APK derlenmesi gerekecek şekilde sürdürülebilir ve bakım maliyeti düşük bir mobil uygulama altyapısı oluşturuldu.
