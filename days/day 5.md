# 🌞 7 Temmuz 2026 Salı

**Django Projesinin Sunucuya Aktarılması ve Hata Analizi**

Bugün hazırladığım Django tabanlı e-ticaret sitesini DeHost sunucusunda yayınlamaya çalıştım. Proje dosyalarını GitHub üzerinden sunucuya aktardım. Sunucuda Django uygulamasının çalışması için gerekli ortam ve veritabanı ayarlarını inceledim.  

Site arayüzü yayınlandı ancak sipariş oluşturma bölümünde hata oluştu. Sorunun kaynağını belirlemek için API adreslerini kontrol ettim. Ürün API’sinin çalıştığını fakat sunucudaki veritabanında ürün bulunmadığı için boş sonuç döndürdüğünü tespit ettim. Arayüzde görünen örnek ürünlerin sunucu veritabanında kayıtlı olmaması nedeniyle sipariş oluşturulamıyordu.  

Bu süreçte:
- Django API adreslerini test ettim.
- Sunucu yönlendirmelerini ve alan adı bağlantısını kontrol ettim.
- DNS kaynaklı erişim problemlerini inceledim.
- PostgreSQL, SQLite ve SQL Server arasındaki farkları araştırdım.
- Veritabanı tablolarının oluşturulması için migration işlemlerini değerlendirdim.
- Örnek ürünlerin canlı veritabanına eklenmesi gerektiğini belirledim.
- Sipariş isteğinin JSON yerine HTML hata sayfası döndürdüğünü tespit ettim.
- Canlı ortam değişkenleri, güvenilir alan adları ve güvenlik ayarlarını kontrol ettim.
- E-posta bildirimi ve yönetim panelinin sunucudaki çalışma durumunu inceledim.

Çalışma sonunda, yalnızca site dosyalarının sunucuya aktarılmasının yeterli olmadığını; veritabanı, alan adı, güvenlik, e-posta ve sunucu yönlendirme ayarlarının da canlı ortama uygun şekilde yapılandırılması gerektiğini öğrendim.

















