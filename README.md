# SmartBooking

# 📌 SmartBook 

## 📝 Proje Hakkında

SmartBook , hizmet sağlayıcıların (kuaför, doktor, eğitmen vb.) ve müşterilerin kullanabileceği, tamamen backend tabanlı bir randevu yönetim sistemidir.

Bu proje:

CV ve portföyde production-ready backend API olarak yer alması
Mülakatlarda teknik mimari, güvenlik, veri modeli ve API tasarımı örneği olarak kullanılması
Spring Boot, PostgreSQL, JWT, Docker gibi teknolojilerin gerçekçi bir senaryoda uygulanması amacıyla geliştirilmiştir.

## 🙌🏻 Hedefler

Local ve Docker üzerinde çalışabilen, production-ready bir backend API oluşturmak
Swagger UI ile dokümante edilmiş API sunmak
GitHub’da clean commit geçmişi, README ve deploy edilmiş demo linki bulundurmak
Proje sürecini anlatan Medium yazı serisi (3 parça) yayınlamak

## 🛠️ Teknik Özellikler

1. Kullanıcı Yönetimi

Kayıt ve giriş (JWT access + refresh token)
Rol bazlı erişim:
USER → kendi randevularını görebilir, düzenleyebilir
ADMIN → tüm kullanıcı ve randevuları görebilir, yönetebilir
2. Randevu (Appointment) Yönetimi

Randevu oluşturma, güncelleme, silme
Çakışma kontrolü (aynı saat aralığında iki randevu olamaz)
Tarih validasyonu (başlangıç tarihi bitişten önce olmalı)
3. Veri Modeli

User (id, name, email, password, roles)
Role (id, name)
Appointment (id, title, startAt, endAt, description, user_id)
4. API Özellikleri

RESTful API
DTO (Data Transfer Object) kullanımı
Validasyon (Spring Validation)
Global exception handling (tek tip hata formatı)
Swagger ile otomatik dokümantasyon

5. Güvenlik


JWT tabanlı authentication
Spring Security ile authorization
Şifrelerin BCrypt ile hashlenmesi

6. Diğer

PostgreSQL veritabanı
Flyway migration (versiyon kontrolü)
Docker + docker-compose (app + db)
JUnit + MockMvc ile unit & integration testler
Scheduler ile otomatik görev (ör: randevu hatırlatma)

## 👩🏻‍💻 Kullanılan Teknolojiler

Java 17
Spring Boot 3.x
Spring Data JPA
Spring Security
PostgreSQL
JWT
Lombok
Swagger / Springdoc OpenAPI
Flyway
Docker & docker-compose
JUnit + MockMvc