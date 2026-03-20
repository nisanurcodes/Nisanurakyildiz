# Nisa Nur Akyıldız'ın Web Frontend Görevleri
**Front-end Test Videosu:** [Link buraya eklenecek](https://example.com)

## 1. Üye Olma (Kayıt) Sayfası
- **API Endpoint:** `POST /auth/register`
- **Görev:** Kullanıcının StudyTrack sistemine kayıt olabilmesi için web sayfası tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Responsive kayıt formu (desktop ve mobile uyumlu)
  - Ad input alanı (`autocomplete="given-name"`)
  - Soyad input alanı (`autocomplete="family-name"`)
  - Email input alanı (`type="email"`, `autocomplete="email"`)
  - Şifre input alanı (`type="password"`, şifre gücü göstergesi)
  - Şifre tekrar input alanı
  - "Kayıt Ol" butonu
  - "Zaten hesabın var mı? Giriş Yap" linki
  - Loading spinner
  - Ortalanmış form container (card veya centered layout)
- **Form Validasyonu:**
  - HTML5 form validation (`required`, `minlength`)
  - JavaScript real-time validation
  - Email format kontrolü
  - Şifre en az 8 karakter olmalıdır
  - Şifre büyük harf, küçük harf ve rakam içermelidir
  - Şifre eşleşme kontrolü yapılmalıdır
  - Ad ve soyad boş bırakılamaz
  - Tüm alanlar geçerli olmadan buton disabled olur
  - Client-side ve server-side validation desteklenir
- **Kullanıcı Deneyimi:**
  - Hata mesajları ilgili input alanının altında gösterilir
  - Başarılı kayıt sonrası success notification gösterilir
  - Kullanıcı otomatik olarak giriş sayfasına yönlendirilir
  - Aynı email ile kayıt durumunda kullanıcı dostu hata mesajı gösterilir
  - Çift tıklama ile tekrar form gönderimi engellenir
  - Keyboard navigation desteği sağlanır
  - Accessible form labels ve ARIA attributes kullanılır
- **Teknik Detaylar:**
  - Framework: React / Vue / Angular veya Vanilla JS
  - Form library: React Hook Form, Formik veya native HTML5
  - State management (form state, loading state, error state)
  - Routing ile giriş sayfasına geçiş
  - Responsive tasarım
  - Accessibility standartlarına uygun geliştirme

## 2. Giriş Yapma Sayfası
- **API Endpoint:** `POST /auth/login`
- **Görev:** Kullanıcının hesabına giriş yapabilmesi için web sayfası tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Responsive giriş formu
  - Email input alanı
  - Şifre input alanı
  - "Giriş Yap" butonu
  - "Hesabın yok mu? Kayıt Ol" linki
  - "Şifremi Unuttum" bağlantısı (opsiyonel)
  - Loading spinner
  - Form container
- **Form Validasyonu:**
  - Email alanı zorunludur
  - Şifre alanı zorunludur
  - Email formatı geçerli olmalıdır
  - Form geçerli olmadan giriş butonu pasif olabilir
- **Kullanıcı Deneyimi:**
  - Başarılı giriş sonrası dashboard sayfasına yönlendirme yapılır
  - Hatalı girişte kullanıcıya anlamlı hata mesajı gösterilir
  - Form gönderimi sırasında buton devre dışı bırakılır
  - Enter tuşu ile giriş yapılabilir
- **Teknik Detaylar:**
  - Authentication token yönetimi
  - Session/localStorage ile oturum yönetimi
  - Protected routes desteği
  - Login state yönetimi

## 3. Dashboard (Ana Panel) Sayfası
- **API Endpoint:** `GET /courses`, `GET /studyplans`, `GET /tasks`
- **Görev:** Kullanıcının derslerini, çalışma planlarını ve görevlerini özet olarak görebileceği ana panel sayfasının tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Hoş geldin mesajı
  - Ders sayısı kartı
  - Yaklaşan çalışma planları alanı
  - Günlük / haftalık görev listesi
  - İlerleme yüzdesi veya progress bar
  - Hızlı işlem butonları (Ders Ekle, Plan Oluştur, Görev Ekle)
  - Responsive grid/card layout
- **Kullanıcı Deneyimi:**
  - Veriler yüklenirken skeleton loading gösterilir
  - Veri yoksa empty state gösterilir
  - Kullanıcı önemli bilgilere tek ekrandan ulaşabilir
  - Sade ve anlaşılır panel düzeni sağlanır
- **Teknik Detaylar:**
  - Birden fazla endpointten veri çekilir
  - Component bazlı yapı tercih edilir
  - Dashboard state ayrı yönetilir
  - İsteğe bağlı caching uygulanabilir

## 4. Ders Listeleme Sayfası
- **API Endpoint:** `GET /courses`
- **Görev:** Kullanıcının eklediği dersleri listeleyebilmesi için sayfa tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Ders kartları veya tablo görünümü
  - Arama kutusu
  - Filtreleme alanı
  - "Yeni Ders Ekle" butonu
  - Her ders için "Detay", "Düzenle", "Sil" butonları
- **Kullanıcı Deneyimi:**
  - Veri yüklenirken loading durumu gösterilir
  - Ders yoksa empty state gösterilir
  - Kullanıcı dersleri kolayca tarayabilir
  - Responsive görünüm korunur
- **Teknik Detaylar:**
  - API verisi liste yapısında işlenir
  - Search ve filter client-side veya server-side yapılabilir
  - Pagination opsiyonel olarak eklenebilir
  - Liste state’i ayrı yönetilebilir

## 5. Ders Ekleme Sayfası
- **API Endpoint:** `POST /courses`
- **Görev:** Kullanıcının yeni bir ders ekleyebilmesi için sayfa tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Ders adı input alanı
  - Ders kodu input alanı
  - Açıklama textarea alanı
  - Kategori veya renk seçimi (opsiyonel)
  - "Kaydet" butonu
  - "İptal" butonu
- **Form Validasyonu:**
  - Ders adı zorunludur
  - Ders kodu projeye göre zorunlu olabilir
  - Açıklama belirli karakter sınırında olabilir
  - Geçersiz formda kaydet butonu pasif olabilir
- **Kullanıcı Deneyimi:**
  - Başarı durumunda kullanıcıya bildirim gösterilir
  - Ders başarıyla eklendiğinde ders listesine yönlendirme yapılır
  - Hata durumunda kullanıcı dostu mesaj gösterilir
- **Teknik Detaylar:**
  - Controlled form yapısı
  - API success / error state yönetimi
  - Reusable form component kullanımı
  - Routing ile geri dönüş

## 6. Ders Düzenleme Sayfası
- **API Endpoint:** `PUT /courses/{id}`
- **Görev:** Kullanıcının mevcut ders bilgilerini güncelleyebilmesi için sayfa tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Önceden doldurulmuş ders formu
  - Ders adı input alanı
  - Ders kodu input alanı
  - Açıklama alanı
  - "Kaydet" butonu
  - "İptal" butonu
  - Değişiklik göstergesi
- **Form Validasyonu:**
  - Ders adı boş bırakılamaz
  - Gerekli alanlar kontrol edilmelidir
  - Değişiklik yapılmadıysa kaydet butonu pasif olabilir
- **Kullanıcı Deneyimi:**
  - Başarı durumunda success notification gösterilir
  - Hata durumunda açıklayıcı mesaj verilir
  - Kaydedilmemiş değişikliklerde çıkış uyarısı gösterilebilir
- **Teknik Detaylar:**
  - İlk yüklemede ilgili ders bilgisi çekilir
  - Dirty state kontrolü yapılabilir
  - Form state ve API state ayrı yönetilir

## 7. Ders Silme Akışı
- **API Endpoint:** `DELETE /courses/{id}`
- **Görev:** Kullanıcının bir dersi güvenli şekilde silebilmesi için akış tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - "Sil" butonu
  - Onay modalı
  - Uyarı mesajı
  - "Evet, Sil" ve "Vazgeç" butonları
- **Kullanıcı Deneyimi:**
  - Kullanıcıya işlemin geri alınamayacağı belirtilir
  - Başarılı silme sonrası liste güncellenir
  - Hata durumunda kullanıcı bilgilendirilir
- **Akış Adımları:**
  1. Kullanıcı sil butonuna tıklar
  2. Onay modalı açılır
  3. Kullanıcı işlemi onaylarsa silme isteği gönderilir
  4. Başarılıysa liste yenilenir
- **Teknik Detaylar:**
  - Modal/Dialog component kullanımı
  - Optimistic update veya refetch yaklaşımı
  - Error handling yapılır

## 8. Konu Listeleme Sayfası
- **API Endpoint:** `GET /topics`
- **Görev:** Kullanıcının eklediği konuları görüntüleyebilmesi için sayfa tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Konu kartları veya tablo görünümü
  - Arama alanı
  - Ders bazlı filtreleme dropdown’u
  - "Yeni Konu Ekle" butonu
- **Kullanıcı Deneyimi:**
  - Konular ders bazında filtrelenebilir
  - Veri yoksa empty state gösterilir
  - Responsive yapı korunur
- **Teknik Detaylar:**
  - Konular ve dersler ilişkili olarak gösterilebilir
  - Listeleme ve filtreleme state ile yönetilir
  - Gerekirse pagination eklenebilir

## 9. Konu Ekleme Sayfası
- **API Endpoint:** `POST /topics`
- **Görev:** Kullanıcının seçili bir derse yeni konu ekleyebilmesi için sayfa tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Konu adı input alanı
  - Ders seçimi için dropdown
  - Açıklama alanı
  - "Kaydet" butonu
  - "İptal" butonu
- **Form Validasyonu:**
  - Konu adı zorunludur
  - Ders seçimi zorunludur
  - Açıklama opsiyonel olabilir
- **Kullanıcı Deneyimi:**
  - Başarılı eklemede konu listesine dönüş yapılır
  - Hata durumunda kullanıcı dostu mesaj gösterilir
- **Teknik Detaylar:**
  - Dropdown verisi ders endpointinden çekilir
  - Form state yönetimi yapılır
  - Routing ile dönüş sağlanır

## 10. Konu Düzenleme Sayfası
- **API Endpoint:** `PUT /topics/{id}`
- **Görev:** Kullanıcının mevcut konu bilgilerini güncelleyebilmesi için sayfa tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Önceden doldurulmuş konu formu
  - Konu adı input alanı
  - Ders seçimi dropdown’u
  - Açıklama alanı
  - "Kaydet" ve "İptal" butonları
- **Form Validasyonu:**
  - Konu adı boş bırakılamaz
  - Ders seçimi geçerli olmalıdır
- **Kullanıcı Deneyimi:**
  - Güncelleme sonrası başarı mesajı gösterilir
  - Hata oluşursa kullanıcıya açıklayıcı mesaj verilir
- **Teknik Detaylar:**
  - İlgili konu verisi ilk yüklemede çekilir
  - Initial data ve form state ayrı yönetilir
  - Unsaved changes warning eklenebilir

## 11. Çalışma Planı Oluşturma Sayfası
- **API Endpoint:** `POST /studyplans`
- **Görev:** Kullanıcının ders veya konu bazlı çalışma planı oluşturabilmesi için sayfa tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Plan başlığı input alanı
  - Ders veya konu seçimi
  - Tarih seçici
  - Süre alanı
  - Not alanı
  - "Plan Oluştur" butonu
- **Form Validasyonu:**
  - Plan başlığı zorunludur
  - Tarih seçimi zorunludur
  - Süre pozitif değer olmalıdır
- **Kullanıcı Deneyimi:**
  - Başarı durumunda plan listesine yönlendirme yapılır
  - Hatalarda kullanıcı bilgilendirilir
  - Kullanıcı dostu tarih seçimi sağlanır
- **Teknik Detaylar:**
  - Date picker entegrasyonu
  - Form state yönetimi
  - API response handling
  - Routing uygulanır

## 12. Çalışma Planı Listeleme Sayfası
- **API Endpoint:** `GET /studyplans`
- **Görev:** Kullanıcının mevcut çalışma planlarını görüntüleyebilmesi için sayfa tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Plan kartları veya tablo görünümü
  - Tarih bazlı sıralama
  - Filtreleme alanı
  - "Yeni Plan Oluştur" butonu
- **Kullanıcı Deneyimi:**
  - Yaklaşan planlar öne çıkarılabilir
  - Geçmiş planlar ayrı gösterilebilir
  - Veri yoksa empty state gösterilir
- **Teknik Detaylar:**
  - Listeleme ve sıralama yapılır
  - Tarih formatlama uygulanır
  - Responsive yapı korunur

## 13. Görev / İlerleme Takip Sayfası
- **API Endpoint:** `GET /tasks`, `POST /tasks`, `PUT /tasks/{id}`
- **Görev:** Kullanıcının çalışma görevlerini ekleyebilmesi, görüntüleyebilmesi ve tamamlayabilmesi için sayfa tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Görev listesi
  - Yeni görev ekleme alanı
  - Checkbox / tamamlandı işareti
  - İlerleme yüzdesi veya progress bar
  - Filtreleme alanı (tamamlanan / tamamlanmayan)
- **Kullanıcı Deneyimi:**
  - Görev tamamlandığında anlık görsel geri bildirim verilir
  - İlerleme oranı otomatik güncellenir
  - Basit ve motive edici bir arayüz sağlanır
- **Teknik Detaylar:**
  - State management ile görev durumu yönetilir
  - PUT/PATCH ile görev güncelleme yapılabilir
  - İlerleme oranı hesaplanabilir

## 14. Profil Görüntüleme Sayfası
- **API Endpoint:** `GET /users/{userId}`
- **Görev:** Kullanıcının profil bilgilerini görüntüleyebilmesi için sayfa tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Responsive profil layout
  - Kullanıcı adı ve soyadı
  - Email bilgisi
  - Hesap oluşturulma tarihi
  - "Profili Düzenle" butonu
- **Kullanıcı Deneyimi:**
  - Loading state, error state ve empty state desteği sağlanır
  - Responsive tasarım uygulanır
  - Bilgiler sade ve okunabilir şekilde gösterilir
- **Teknik Detaylar:**
  - Kullanıcı verisi API’den çekilir
  - Profil düzenleme sayfasına routing yapılır
  - State yönetimi uygulanır

## 15. Profil Düzenleme Sayfası
- **API Endpoint:** `PUT /users/{userId}`
- **Görev:** Kullanıcının profil bilgilerini güncelleyebilmesi için sayfa tasarımı ve implementasyonu
- **UI Bileşenleri:**
  - Ad input alanı
  - Soyad input alanı
  - Email input alanı
  - "Kaydet" butonu
  - "İptal" butonu
  - Değişiklik göstergesi
- **Form Validasyonu:**
  - Email formatı geçerli olmalıdır
  - Ad ve soyad boş bırakılamaz
  - Değişiklik yoksa kaydet butonu disabled olabilir
- **Kullanıcı Deneyimi:**
  - Başarılı güncellemede success notification gösterilir
  - Hata durumunda kullanıcıya bilgi verilir
  - Kaydedilmemiş değişikliklerde uyarı verilebilir
- **Teknik Detaylar:**
  - Form state yönetimi yapılır
  - API entegrasyonu sağlanır
  - Güncelleme sonrası profil sayfasına yönlendirme yapılır
