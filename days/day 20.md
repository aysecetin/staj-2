
# 🌞 29 Temmuz 2026 Çarşamba

## Mobil Uygulamanın Android APK Derlemesi ve Hata Çözümü
- Bugün SürüTakip mobil uygulamasının Android cihazlara kurulabilmesi için APK oluşturma ve derleme çalışmalarını gerçekleştirdim.
- Expo Application Services (EAS) üzerinde mobil uygulama projesini yapılandırdım ve yerel projeyi Expo hesabımdaki @aysecetin/surutakip projesine bağladım.
- Mobil uygulamanın canlı Django API servisine bağlanabilmesi için EXPO_PUBLIC_API_URL ortam değişkenini EAS üzerinde tanımladım. Bu değişkeni Render üzerinde çalışan API adresine yönlendirdim.
- Android uygulamasını mağaza dışında doğrudan telefonlara kurulabilecek APK formatında hazırlamak için EAS preview derleme profilini kullandım. Böylece uygulamanın Play Store’a yüklenmeden bağlantı veya QR kod aracılığıyla indirilebilmesini sağladım.
- İlk Android derleme denemesinde Gradle aşamasında hata aldım. EAS tarafından gösterilen genel hata mesajının yeterli olmaması nedeniyle derleme kayıtlarını ayrıntılı olarak inceledim.
- Hatanın Android kaynak işleme aşamasında oluştuğunu belirledim. Gradle, açılış ekranında kullanılacak splashscreen_logo adlı görsel kaynağını bulamadığı için APK üretimi tamamlanamıyordu.
- Sorunu çözmek için mobil uygulamanın app.json dosyasındaki Expo Splash Screen yapılandırmasını düzenledim. Mevcut splash-icon.png görselini açılış ekranı görseli olarak açıkça tanımladım. Görsel genişliğini, yeniden boyutlandırma biçimini ve arka plan rengini yapılandırdım.
- Düzenlemenin ardından geçici bir Android projesi oluşturarak eksik olan splashscreen_logo.png kaynaklarının farklı ekran yoğunlukları için doğru biçimde üretildiğini kontrol ettim.
- Yaptığım değişikliklerden sonra TypeScript tip kontrolünü ve kod kalite kontrolünü çalıştırdım. Her iki kontrolü de hatasız tamamladım. Expo yapılandırmasının Android projesine doğru aktarıldığını doğruladım.
- Hata düzeltmesini ayrı bir Git commit’i olarak kaydettim ve feature/mobile-foundation branch’ine gönderdim. Commit mesajını yapılan düzeltmeyi açıklayacak şekilde hazırladım.
- Yeni Android derlemesini temiz önbellekle tekrar başlattım. Böylece önceki başarısız derlemeden kalan dosyaların yeni derlemeyi etkilemesini önledim.

İkinci derleme başarıyla tamamlandı ve uygulamanın Android APK dosyası oluşturuldu. Expo tarafından verilen indirme bağlantısı sayesinde uygulamanın Android telefonlara kurulabilir hale gelmesini sağladım.

Derleme sonunda uygulamayı bilgisayardaki Android emülatörüne kurma işlemini denedim. Bilgisayarda Android Studio ve ADB bulunmadığı için emülatör kurulumu gerçekleştirilemedi. Bu hatanın APK derlemesiyle ilgili olmadığını, yalnızca bilgisayarda emülatör altyapısının bulunmamasından kaynaklandığını tespit ettim.

Sonuç olarak SürüTakip mobil uygulamasının Android APK derleme hatasını giderdim. Uygulamayı Play Store’a yüklemeden, doğrudan indirme bağlantısı üzerinden Android cihazlara kurulabilecek hale getirdim.
