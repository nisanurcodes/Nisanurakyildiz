# StudyTrack Web Frontend Görevleri
**Front-end Test Videosu:** [Link buraya eklenecek](https://example.com)

## 1. Üye Olma (Kayıt) Sayfası
- **API Endpoint:** `POST /auth/register`
- **Görev:** Kullanıcının sisteme kayıt olabilmesi için web sayfası tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Responsive kayıt formu
  - Ad input alanı
  - Soyad input alanı
  - Email input alanı (`type="email"`)
  - Şifre input alanı (`type="password"`)
  - Şifre tekrar input alanı
  - "Kayıt Ol" butonu
  - "Zaten hesabın var mı? Giriş Yap" linki
  - Loading spinner
  - Form container (card yapısı veya ortalanmış form alanı)
- **Form Validasyonu:**
  - Tüm alanlar zorunlu
  - Email format kontrolü
  - Şifre en az 8 karakter olmalı
  - Şifre ve şifre tekrar eşleşmeli
  - Ad ve soyad boş bırakılamaz
  - Tüm alanlar geçerli olmadan buton disabled olur
- **Kullanıcı Deneyimi:**
  - Hata mesajları input altında gösterilir
  - Başarılı kayıt sonrası kullanıcı giriş sayfasına yönlendirilir
  - Hatalı kayıt durumunda kullanıcı dostu hata mesajı gösterilir
  - Çift tıklama ile tekrar gönderim engellenir
  - Klavye ile form kullanımı desteklenir
- **Teknik Detaylar:**
  - React / Vue / Angular veya Vanilla JS ile geliştirilebilir
  - Form state, loading state ve error state yönetimi yapılır
  - Client-side ve server-side validation desteklenir
  - Routing ile giriş sayfasına geçiş sağlanır
  - Responsive tasarım uygulanır

## 2. Giriş Yapma Sayfası
- **API Endpoint:** `POST /auth/login`
- **Görev:** Kullanıcının hesabına giriş yapabilmesi için web sayfası tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Responsive giriş formu
  - Email input alanı
  - Şifre input alanı
  - "Giriş Yap" butonu
  - "Hesabın yok mu? Kayıt Ol" linki
  - Şifremi unuttum bağlantısı (opsiyonel)
  - Loading spinner
- **Form Validasyonu:**
  - Email boş bırakılamaz
  - Şifre boş bırakılamaz
  - Email formatı geçerli olmalı
  - Alanlar geçerli olmadan giriş butonu pasif olabilir
- **Kullanıcı Deneyimi:**
  - Başarılı giriş sonrası dashboard sayfasına yönlendirme
  - Hatalı girişte kullanıcıya anlamlı uyarı mesajı gösterilir
  - Enter tuşu ile form gönderimi desteklenir
  - Giriş işlemi sırasında buton devre dışı bırakılır
- **Teknik Detaylar:**
  - Authentication token saklama işlemi yapılır
  - Session/localStorage yönetimi sağlanır
  - State management ile kullanıcı oturumu takip edilir
  - Route guard ile korumalı sayfalara erişim kontrol edilir

## 3. Dashboard (Ana Panel) Sayfası
- **API Endpoint:** `GET /courses`, `GET /studyplans`, `GET /tasks`
- **Görev:** Kullanıcının derslerini, çalışma planlarını ve görevlerini genel olarak görebileceği ana panel sayfasının tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Hoş geldin mesajı
  - Ders kartları
  - Yaklaşan çalışma planları listesi
  - Tamamlanacak görevler listesi
  - Hızlı işlem butonları (Ders Ekle, Plan Oluştur vb.)
  - Responsive grid yapı
- **Kullanıcı Deneyimi:**
  - Veriler yüklenirken skeleton/loading alanı gösterilir
  - Veri yoksa empty state gösterilir
  - Sayfa kullanıcı için özet bilgi sunar
  - Mobil ve masaüstü uyumlu yapı bulunur
- **Teknik Detaylar:**
  - Birden fazla endpointten veri çekilebilir
  - Component bazlı yapı kullanılır
  - State management ile dersler, planlar ve görevler yönetilir
  - Gerekirse caching uygulanır

## 4. Ders Listeleme Sayfası
- **API Endpoint:** `GET /courses`
- **Görev:** Kullanıcının eklediği tüm dersleri görüntüleyebileceği sayfa tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Ders kartları veya tablo görünümü
  - Arama çubuğu
  - Filtreleme alanı
  - "Yeni Ders Ekle" butonu
  - Her ders için "Detay", "Düzenle", "Sil" butonları
- **Kullanıcı Deneyimi:**
  - Boş durumda ders bulunamadı mesajı gösterilir
  - Yüklenme sırasında loading göstergesi yer alır
  - Liste responsive şekilde görüntülenir
  - Kullanıcı dersleri hızlıca tarayabilir
- **Teknik Detaylar:**
  - API’den çekilen veri liste halinde işlenir
  - Arama ve filtreleme client-side veya server-side yapılabilir
  - Sayfalama (pagination) opsiyonel olarak eklenebilir

## 5. Ders Ekleme Sayfası
- **API Endpoint:** `POST /courses`
- **Görev:** Kullanıcının yeni ders ekleyebilmesi için sayfa tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Ders adı input alanı
  - Ders kodu input alanı
  - Açıklama textarea alanı
  - Kredi bilgisi input alanı (opsiyonel)
  - Renk veya kategori seçimi (opsiyonel)
  - "Kaydet" butonu
  - "İptal" butonu
- **Form Validasyonu:**
  - Ders adı zorunlu
  - Ders kodu boş bırakılamaz (opsiyonel kurala göre)
  - Alanlar geçerli değilse kaydet butonu pasif olabilir
- **Kullanıcı Deneyimi:**
  - Başarılı ekleme sonrası ders listesine yönlendirme
  - Hata durumunda kullanıcı bilgilendirilir
  - Form gönderilirken loading durumu gösterilir
- **Teknik Detaylar:**
  - Form state yönetimi
  - API isteği sonrası başarı/hata kontrolü
  - Routing ile ders listesine dönüş
  - Reusable input component yapısı kullanılabilir

## 6. Ders Düzenleme Sayfası
- **API Endpoint:** `PUT /courses/{id}`
- **Görev:** Kullanıcının mevcut ders bilgilerini düzenleyebilmesi için sayfa tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Mevcut bilgilerle doldurulmuş form
  - Ders adı input alanı
  - Ders kodu input alanı
  - Açıklama alanı
  - "Kaydet" butonu
  - "İptal" butonu
- **Form Validasyonu:**
  - Ders adı boş olamaz
  - Gerekli alanlar doğrulanmalıdır
  - Değişiklik yoksa kaydet butonu pasif olabilir
- **Kullanıcı Deneyimi:**
  - Başarılı güncelleme sonrası başarı mesajı gösterilir
  - Kullanıcı ders detayına veya ders listesine yönlendirilir
  - Sayfadan çıkarken kaydedilmemiş değişiklikler için uyarı verilebilir
- **Teknik Detaylar:**
  - İlk veri yükleme için ilgili ders bilgisi çekilir
  - Dirty state kontrolü yapılabilir
  - Form state ve API state ayrı yönetilir

## 7. Ders Silme Akışı
- **API Endpoint:** `DELETE /courses/{id}`
- **Görev:** Kullanıcının bir dersi silebilmesi için güvenli silme akışı tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - "Sil" butonu
  - Onay modalı
  - Uyarı mesajı
  - "Evet, Sil" ve "Vazgeç" butonları
- **Kullanıcı Deneyimi:**
  - Kullanıcıya bu işlemin geri alınamayacağı açıkça belirtilir
  - Başarılı silme sonrası ders listesi güncellenir
  - Hata durumunda kullanıcıya bilgi verilir
- **Akış Adımları:**
  1. Kullanıcı sil butonuna tıklar
  2. Onay modalı açılır
  3. Kullanıcı işlemi onaylarsa silme isteği gönderilir
  4. Başarılıysa liste güncellenir
- **Teknik Detaylar:**
  - Modal bileşeni kullanılır
  - Optimistic UI veya yeniden veri çekme uygulanabilir
  - Hata yönetimi sağlanır

## 8. Konu Listeleme Sayfası
- **API Endpoint:** `GET /topics`
- **Görev:** Kullanıcının eklediği tüm konuları listeleyebilmesi için sayfa tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Konu kartları veya tablo görünümü
  - Filtreleme alanı
  - Arama çubuğu
  - "Yeni Konu Ekle" butonu
- **Kullanıcı Deneyimi:**
  - Kullanıcı konuları derslere göre filtreleyebilir
  - Veri yoksa boş durum mesajı gösterilir
  - Responsive yapı sağlanır
- **Teknik Detaylar:**
  - Konular ilgili derslerle ilişkilendirilebilir
  - Listeleme ve filtreleme yapılır
  - State yönetimi uygulanır

## 9. Konu Ekleme Sayfası
- **API Endpoint:** `POST /topics`
- **Görev:** Kullanıcının belirli bir derse yeni konu ekleyebilmesi için sayfa tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Konu adı input alanı
  - İlgili ders seçimi için dropdown
  - Açıklama alanı
  - "Kaydet" butonu
- **Form Validasyonu:**
  - Konu adı boş bırakılamaz
  - Ders seçimi zorunludur
- **Kullanıcı Deneyimi:**
  - Başarılı ekleme sonrası konu listesine dönüş yapılır
  - Hatalarda kullanıcı dostu mesajlar gösterilir
- **Teknik Detaylar:**
  - Dropdown için ders listesi API’den çekilir
  - Form submit sonrası yönlendirme yapılır

## 10. Çalışma Planı Oluşturma Sayfası
- **API Endpoint:** `POST /studyplans`
- **Görev:** Kullanıcının ders veya konu bazlı çalışma planı oluşturabilmesi için sayfa tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Plan başlığı input alanı
  - Ders veya konu seçimi
  - Tarih seçici
  - Süre bilgisi alanı
  - Not alanı
  - "Plan Oluştur" butonu
- **Form Validasyonu:**
  - Plan başlığı zorunlu
  - Tarih seçimi zorunlu
  - Süre pozitif değer olmalı
- **Kullanıcı Deneyimi:**
  - Başarılı işlem sonrası plan listesine yönlendirme
  - Hata durumunda uyarı mesajı gösterimi
  - Kullanıcı dostu tarih seçimi
- **Teknik Detaylar:**
  - Date picker entegrasyonu
  - Form state yönetimi
  - API entegrasyonu ve yönlendirme

## 11. Çalışma Planı Listeleme Sayfası
- **API Endpoint:** `GET /studyplans`
- **Görev:** Kullanıcının oluşturduğu çalışma planlarını görüntüleyebilmesi için sayfa tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Plan kartları veya tablo
  - Tarihe göre sıralama
  - Filtreleme alanı
  - "Plan Oluştur" butonu
- **Kullanıcı Deneyimi:**
  - Yaklaşan planlar vurgulanabilir
  - Geçmiş planlar ayrı gösterilebilir
  - Veri yoksa empty state gösterilir
- **Teknik Detaylar:**
  - Listeleme, sıralama ve filtreleme desteği
  - Tarih formatlama işlemleri
  - Responsive tasarım

## 12. Görev / İlerleme Takip Sayfası
- **API Endpoint:** `GET /tasks`, `POST /tasks`, `PUT /tasks/{id}`
- **Görev:** Kullanıcının çalışma görevlerini ekleyebilmesi, görüntüleyebilmesi ve tamamlayabilmesi için sayfa tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Görev listesi
  - Checkbox veya tamamlandı butonu
  - Yeni görev ekleme alanı
  - İlerleme yüzdesi göstergesi
  - Filtreleme (tamamlanan / tamamlanmayan)
- **Kullanıcı Deneyimi:**
  - Görev tamamlandığında anlık görsel geri bildirim verilir
  - İlerleme barı güncellenir
  - Kullanıcı motivasyonu için sade ve anlaşılır yapı sunulur
- **Teknik Detaylar:**
  - State management ile görev durumu yönetilir
  - PATCH/PUT ile görev durumu güncellenebilir
  - İlerleme oranı hesaplanabilir

## 13. Profil Görüntüleme Sayfası
- **API Endpoint:** `GET /users/{userId}`
- **Görev:** Kullanıcının kendi profil bilgilerini görüntüleyebilmesi için sayfa tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Profil kartı
  - Ad soyad bilgisi
  - Email bilgisi
  - Hesap oluşturulma tarihi
  - "Profili Düzenle" butonu
- **Kullanıcı Deneyimi:**
  - Loading ve error state desteği
  - Responsive tasarım
  - Profil bilgileri sade şekilde gösterilir
- **Teknik Detaylar:**
  - Kullanıcı verisi API’den çekilir
  - Profil düzenleme sayfasına routing yapılır
  - State yönetimi uygulanır

## 14. Profil Düzenleme Sayfası
- **API Endpoint:** `PUT /users/{userId}`
- **Görev:** Kullanıcının profil bilgilerini güncelleyebilmesi için sayfa tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Ad input alanı
  - Soyad input alanı
  - Email input alanı
  - "Kaydet" butonu
  - "İptal" butonu
- **Form Validasyonu:**
  - Email formatı geçerli olmalı
  - Ad ve soyad boş bırakılamaz
- **Kullanıcı Deneyimi:**
  - Başarı mesajı gösterilir
  - Hata durumunda kullanıcıya bilgi verilir
  - Kaydedilmemiş değişiklikler için uyarı verilebilir
- **Teknik Detaylar:**
  - Form state yönetimi
  - API entegrasyonu
  - Güncelleme sonrası profil sayfasına yönlendirme
