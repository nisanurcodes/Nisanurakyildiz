Web Frontend Görev Dağılımı

Web Frontend Adresi:
👉 https://studytrack-frontend-d1dp.vercel.app/

🎥 Frontend Test Videosu:
👉 https://youtu.be/b-BqF04aNW8?si=nMeKQuRkDW5CSIrK

Bu dokümanda, StudyTrack web uygulamasının kullanıcı arayüzü (UI) ve kullanıcı deneyimi (UX) ile ilgili görevler listelenmektedir. Proje bireysel olarak geliştirildiği için tüm web frontend görevleri tek kişi tarafından yürütülmektedir. Bu görevler; sayfa tasarımı, implementasyon, form yönetimi, kullanıcı etkileşimleri ve API entegrasyonunu kapsamaktadır.

---

## Web Frontend Görevleri

1. [Nisa Nur Akyıldız'ın Web Frontend Görevleri](Nisa-Nur-Akyildiz/Nisa-Nur-Akyildiz-Web-Frontend-Gorevleri.md)

---

## Genel Web Frontend Prensipleri

### 1. Responsive Tasarım
- **Mobile-First Approach:** Önce mobil görünüm, ardından tablet ve desktop düzeni
- **Breakpoints:**
  - Mobile: `< 768px`
  - Tablet: `768px - 1024px`
  - Desktop: `> 1024px`
- **Flexible Layouts:** CSS Grid ve Flexbox kullanımı
- **Responsive Images:** Uygun boyutlandırma ve ölçeklenebilir görseller
- **Touch-Friendly:** Buton ve tıklanabilir alanların yeterli boyutta olması

### 2. Tasarım Sistemi
- **UI Framework / Library:** Bootstrap, Tailwind CSS, Material UI veya custom CSS
- **Renk Paleti:** Tutarlı ve sade bir renk sistemi
- **Tipografi:** Okunabilir ve tutarlı font kullanımı
- **Spacing:** Düzenli padding ve margin sistemi
- **Iconography:** Uyumlu ikon seti kullanımı
- **Reusable Components:** Yeniden kullanılabilir buton, input, modal, card bileşenleri

### 3. Performans Optimizasyonu
- **Code Splitting:** Sayfa bazlı veya bileşen bazlı ayırma
- **Lazy Loading:** Sayfa ve bileşenlerin ihtiyaç halinde yüklenmesi
- **Minification:** CSS ve JavaScript küçültme
- **Compression:** Gzip/Brotli desteği
- **Caching:** Tarayıcı önbellekleme ve uygun veri saklama stratejileri
- **Bundle Size Optimization:** Gereksiz kodların kaldırılması

### 4. Erişilebilirlik (Accessibility)
- **Semantic HTML:** Doğru HTML etiketlerinin kullanımı
- **Keyboard Navigation:** Tab ile gezilebilir yapı
- **ARIA Labels:** Gerekli alanlarda ekran okuyucu desteği
- **Color Contrast:** Okunabilir kontrast oranları
- **Focus States:** Görünür odaklanma stilleri
- **Form Labels:** Tüm formlarda açık ve erişilebilir etiket yapısı

### 5. Browser Uyumluluğu
- **Desteklenen Tarayıcılar:** Chrome, Firefox, Safari, Edge
- **Responsive Testing:** Farklı ekran boyutlarında test
- **Fallback Yapılar:** Gerekli yerlerde alternatif çözümler
- **Feature Detection:** Tarayıcı desteğine göre kontrollü kullanım

### 6. State Management
- **Local State:** Bileşen bazlı state kullanımı
- **Global State:** Gerekirse Context API, Redux, Zustand vb.
- **Form State:** React Hook Form, Formik veya native form yönetimi
- **Server State:** API’den gelen verilerin yönetimi

### 7. Routing
- **Client-Side Routing:** React Router / Vue Router / Angular Router
- **Protected Routes:** Giriş gerektiren sayfalar için erişim kontrolü
- **404 Page:** Bulunamayan sayfalar için özel ekran
- **Navigation Structure:** Anlaşılır ve tutarlı yönlendirme yapısı

### 8. API Entegrasyonu
- **HTTP Client:** Axios, Fetch API veya benzeri yapı
- **Request Handling:** İstek öncesi token ekleme, validation ve loading yönetimi
- **Response Handling:** Başarı ve hata durumlarının ayrıştırılması
- **Error Handling:** Merkezi hata yönetimi
- **Loading States:** Sayfa veya bileşen bazlı yüklenme göstergeleri

### 9. Form ve Kullanıcı Etkileşimi
- **Validation:** Client-side ve server-side doğrulama
- **Error Messages:** Kullanıcı dostu hata mesajları
- **Success Feedback:** Başarı durumunda toast/snackbar/mesaj gösterimi
- **Disabled States:** Geçersiz veya eksik formda butonların pasif olması
- **Confirmation Flows:** Silme gibi işlemlerde onay mekanizması

### 10. Testing
- **Unit Tests:** Temel bileşen testleri
- **Integration Tests:** Form ve sayfa akışlarının testi
- **E2E Tests:** Kritik kullanıcı senaryolarının testi
- **Accessibility Tests:** Form ve gezinme erişilebilirliği kontrolü
- **Responsive Tests:** Mobil/tablet/desktop görünüm doğrulaması

### 11. Build ve Deployment
- **Build Tool:** Vite, Webpack veya benzeri yapı
- **Environment Variables:** `.env` ile ortam değişkenlerinin yönetimi
- **Deployment:** Vercel, Netlify, GitHub Pages veya benzeri platformlar
- **CI/CD:** Gerekirse GitHub Actions ile otomatik build/deploy süreci

### 12. StudyTrack Projesine Özel Frontend Hedefleri
- **Authentication Pages:** Kayıt olma ve giriş yapma sayfaları
- **Dashboard:** Kullanıcının ders, plan ve görev özetlerini görmesi
- **Course Management:** Ders ekleme, listeleme, düzenleme ve silme
- **Topic Management:** Konu ekleme, listeleme, düzenleme ve silme
- **Study Plan Management:** Çalışma planı oluşturma ve görüntüleme
- **Task / Progress Tracking:** Görev takibi ve ilerleme gösterimi
- **Profile Pages:** Profil görüntüleme ve düzenleme

---

## Klasör Yapısı Önerisi

```text
docs/
├── Web-Frontend-Gorev-Dagilimi.md
└── Nisa-Nur-Akyildiz/
    └── Nisa-Nur-Akyildiz-Web-Frontend-Gorevleri.md
