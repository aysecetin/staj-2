# SESSION 4 — Yeni Oyun Tasarımı Güncellemesi

Bu doküman, önceki Session Handoff dosyalarına ek olarak uygulanacak yeni oyun tasarım kararlarını içerir.

Bu dokümandaki maddeler mevcut sistemin üzerine eklenecek ve bazı eski tasarım kararlarının yerini alacaktır.

---

# 1. Temel Oyun Mantığı Değişmeyecek

Oyunun ana mekaniği korunacaktır.

Oyuncu;

- LEGO parçalarını oluşturmayacak,
- tahtaya yeni parça yerleştirmeyecek,
- parça döndürmeyecek.

Bölüm başladığında tüm LEGO parçaları tahtada hazır bulunacaktır.

Oyuncu her parçayı parmağıyla sürükleyerek yalnızca hareket ettirecektir.

Amaç;

her LEGO parçasını kendi renk kapısından geçirerek tahtadan tamamen çıkarmaktır.

Tüm parçalar çıkarıldığında bölüm tamamlanacaktır.

---

# 2. Yeni LEGO Parça Havuzu

Mevcut parçalara ek olarak daha fazla şekil kullanılacaktır.

Desteklenecek temel parçalar:

- 1x1
- 1x2
- 2x1
- 1x3
- 3x1
- 2x2
- Küçük L
- Büyük L
- T
- Artı (+)

Bu parçaların;

- 90°
- 180°
- 270°

rotasyonları kullanılacaktır.

Gerekli görülen parçalarda sağ-sol aynalanmış versiyonlar da üretilebilir.

Bölüm oluşturucu bu parçaları rastgele değil, çözülebilir bulmacalar oluşturacak şekilde kullanacaktır.

---

# 3. Yeni Çok Katmanlı Renk Sistemi

Oyuna yeni bir LEGO türü eklenecektir.

Bu parçalar tek renk yerine iki katmandan oluşacaktır.

Örneğin;

Dış katman:
- Mavi

İç katman:
- Turuncu

Bu durumda çözüm sırası zorunlu olacaktır.

Akış şu şekilde çalışacaktır.

1. Parça önce mavi kapıya götürülür.
2. Mavi dış katman kaybolur.
3. Parça tamamen turuncuya dönüşür.
4. Daha sonra turuncu kapıya götürülür.
5. Turuncu kapıdan çıkarak tahtadan tamamen silinir.

Yani tek LEGO parçası iki farklı kapıdan geçmek zorundadır.

Bu sistem yalnızca iki katmanlı parçalar için geçerlidir.

Normal tek renkli parçalar mevcut davranışını koruyacaktır.

---

# 4. Yeni Board Sistemi

Board artık yalnızca dikdörtgen veya kare olmayacaktır.

Her bölüm kendine ait farklı bir oyun alanına sahip olabilir.

Örneğin;

- girintiler
- çıkıntılar
- dar koridorlar
- asimetrik kenarlar
- özel şekilli oyun alanları

kullanılabilecektir.

Board şekli bulmacanın bir parçası olacaktır.

---

# 5. Girinti ve Çıkıntılar

Board üzerindeki girinti ve çıkıntılar yalnızca görsel amaçlı değildir.

Bu yapılar;

- hareket alanını daraltır,
- uzun parçaların dönüşünü zorlaştırır,
- bazı parçaların sıkışmasına neden olur,
- çözüm sırasını değiştirir.

Böylece bölümün zorluğu yalnızca parça sayısıyla değil, board geometrisiyle de belirlenmiş olur.

---

# 6. Yeni Bulmaca Tasarımı

Yeni bölümler hazırlanırken aşağıdaki değişkenler birlikte kullanılacaktır.

- farklı LEGO şekilleri
- farklı board şekilleri
- girintiler
- çıkıntılar
- dar geçitler
- engeller
- sandık sistemi
- tek renkli parçalar
- iki katmanlı parçalar

Her bölüm farklı bir çözüm mantığına sahip olmalıdır.

---

# 7. Bölüm Tasarım Kuralları

Yeni bölüm üreticisi aşağıdaki kurallara uymalıdır.

- Her bölüm deterministik olmalıdır.
- Her bölüm çözülebilir olmalıdır.
- Hiçbir parça çözümsüz sıkışmamalıdır.
- Kapıların önü tamamen açık olmalıdır.
- İki katmanlı parçalarda kapı sırası doğru planlanmalıdır.
- Board geometrisi parçaların fiziksel hareketine uygun olmalıdır.
- Oyuncu hiçbir zaman engellerin veya diğer parçaların içinden geçememelidir.

---

# 8. Tasarım Hedefi

Yeni sistem ile amaç;

oyunun sadece "parçayı kapıya götür" mantığında kalmamasıdır.

Artık oyuncu;

- hangi parçayı önce hareket ettireceğini,
- hangi kapıyı önce kullanacağını,
- dar alanlardan nasıl çıkacağını,
- çift katmanlı parçaları hangi sırayla çözeceğini

planlamak zorunda kalacaktır.

Bu sayede ilerleyen bölümlerde zorluk doğal şekilde artacak, tekrar hissi azalacak ve bulmaca çeşitliliği önemli ölçüde yükselecektir.
