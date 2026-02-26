Ders Takip Uygulaması Gereksinim Analizi

Ders ve konu takip uygulaması için gereksinim analizi dokümanı.

👤 Kullanıcı İşlemleri
1. Kayıt Olma

API Metodu: POST /auth/register

Açıklama: Kullanıcının e-posta ve şifre belirleyerek sisteme yeni bir hesap oluşturmasını sağlar.

2. Giriş Yapma

API Metodu: POST /auth/login

Açıklama: Kullanıcının sisteme giriş yapmasını sağlar ve kimlik doğrulama işlemi gerçekleştirilir.

3. Çıkış Yapma

API Metodu: POST /auth/logout

Açıklama: Kullanıcının aktif oturumunu sonlandırmasını sağlar.

4. Profil Görüntüleme

API Metodu: GET /users/{userId}

Açıklama: Kullanıcının profil bilgilerini görüntülemesini sağlar. Kullanıcının sisteme giriş yapmış olması gerekir.

5. Profil Güncelleme

API Metodu: PUT /users/{userId}

Açıklama: Kullanıcının ad ve e-posta gibi profil bilgilerini güncellemesini sağlar. Kullanıcı yalnızca kendi bilgilerini güncelleyebilir.

6. Hesap Silme

API Metodu: DELETE /users/{userId}

Açıklama: Kullanıcının hesabını sistemden kalıcı olarak silmesini sağlar. Bu işlem geri alınamaz.

📚 Ders İşlemleri
7. Ders Ekleme

API Metodu: POST /courses

Açıklama: Kullanıcının yeni bir ders oluşturmasını sağlar.

8. Ders Listeleme

API Metodu: GET /courses

Açıklama: Kullanıcının oluşturduğu tüm dersleri listelemesini sağlar.

9. Ders Güncelleme

API Metodu: PUT /courses/{courseId}

Açıklama: Seçilen dersin adını veya bilgilerini güncellemesini sağlar.

10. Ders Silme

API Metodu: DELETE /courses/{courseId}

Açıklama: Seçilen dersin sistemden silinmesini sağlar.

⏱ Çalışma Oturumu İşlemleri
11. Çalışma Oturumu Başlatma

API Metodu: POST /study-sessions

Açıklama: Kullanıcının yeni bir çalışma oturumu başlatmasını sağlar ve süre takibi başlar.

12. Çalışma Oturumu Sonlandırma

API Metodu: PUT /study-sessions/{sessionId}

Açıklama: Aktif çalışma oturumunu sonlandırır ve toplam süreyi kaydeder.

13. Geçmiş Çalışma Oturumlarını Görüntüleme

API Metodu: GET /study-sessions

Açıklama: Kullanıcının geçmiş çalışma kayıtlarını listelemesini sağlar.

14. Çalışma Kaydı Silme

API Metodu: DELETE /study-sessions/{sessionId}

Açıklama: Seçilen çalışma kaydını sistemden silmesini sağlar.

🤖 AI Çalışma Planı İşlemleri
15. AI ile Çalışma Planı Oluşturma

API Metodu: POST /ai/study-plan

Açıklama: Kullanıcının geçmiş çalışma verilerini analiz ederek kişisel çalışma planı oluşturur.

16. AI Çalışma Planını Görüntüleme

API Metodu: GET /ai/study-plan

Açıklama: Oluşturulan çalışma planının görüntülenmesini sağlar.

17. AI Çalışma Planını Güncelleme

API Metodu: PUT /ai/study-plan

Açıklama: Kullanıcının oluşturulan çalışma planı üzerinde değişiklik yapmasını sağlar.

18. AI Çalışma Planını Silme

API Metodu: DELETE /ai/study-plan

Açıklama: Oluşturulan çalışma planının sistemden silinmesini sağlar.
