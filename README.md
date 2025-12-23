# Hotel Management System (ENG)
CS 202 – Semester Project (Fall 2024)

## Project Overview

This project is a Hotel Management System developed as part of the CS 202 Database Management Systems course.  
The system is implemented using Java (JDBC) and MySQL, and provides a console-based, menu-driven interface for managing hotel operations.

The main objective of the project is to design a 3rd Normal Form (3NF) compliant relational database and to solve system requirements primarily using SQL, rather than Java-based workarounds.

This repository represents an individual fork of a team project, created for version control and personal development purposes.

---

## System Features

- Console (terminal) based menu-driven application
- MySQL database designed in 3NF
- JDBC-based database connectivity
- SQL-driven data operations (DDL & DML)
- Full error handling and user-friendly prompts

---

## User Roles

The system supports the following user types:

### Administrator
- Create, update, and delete rooms
- Manage room status
- View all bookings and housekeeping records
- Generate revenue reports
- Cancel bookings if no payment has been made
- Administrator accounts are predefined in the database

### Receptionist
- View room availability
- Manage booking requests
- Confirm or reject bookings
- Schedule housekeeping tasks

### Guest
- Create room bookings based on availability
- View personal bookings
- Check in after booking confirmation
- Check out after completing payment

### Housekeeping
- View room availability (without guest details)
- View assigned housekeeping schedules
- Update cleaning task status

---

## Database Design

- Designed based on functional dependencies
- Fully normalized to Third Normal Form (3NF)
- Core entities include:
  - Users, Roles
  - Rooms, Room Types
  - Bookings, Payments
  - Housekeeping Schedules
  - Employees
- Referential integrity enforced using foreign keys
- Overbooking is prevented at the database level
- Only clean rooms can be booked

---

## Project Structure

```text
src/main/java/com/example/hotelmanagement
│
├── Entity
│ ├── Users, Roles, Guest, Employee, Administrator
│ ├── Room, Room_Type, Booking, Payments
│ ├── Housekeeping, HousekeepingSchedule
│ └── Reviews, Hotel
│
├── repository
│ ├── UsersRepository
│ ├── RoomRepository
│ ├── BookingRepository
│ ├── PaymentsRepository
│ ├── HousekeepingRepository
│ └── Other repository classes
│
├── services
│ ├── Booking management services
│ ├── Check-in / Check-out services
│ ├── Payment processing
│ ├── Administrator management services
│ └── Housekeeping scheduling and task management
│
├── ConsoleMenu.java
├── DatabaseConnection.java
└── Main.java
```

---

## Technologies Used

- Java
- MySQL
- JDBC
- Gradle
- SQL (DDL & DML)

---

## How to Run

1. Create the database using `DDL.sql`
2. Insert sample data using `DML.sql`
3. Configure database credentials in `DatabaseConnection.java`
4. Run `Main.java`
5. Use the console menu to interact with the system

---

# Hotel Yönetim Sistemi (Türkçe)
CS 202 – Dönem Projesi (Güz 2024)

## Proje Tanımı

Bu proje, **CS 202 Veritabanı Yönetim Sistemleri** dersi kapsamında geliştirilmiş bir **Otel Yönetim Sistemi**dir.  
Sistem, **Java (JDBC)** ve **MySQL** kullanılarak geliştirilmiş olup, **konsol (terminal) tabanlı ve menü yönlendirmeli** bir yapıya sahiptir.

Projenin temel amacı, **3. Normal Form (3NF)** kurallarına uygun bir ilişkisel veritabanı tasarlamak ve sistem gereksinimlerini ağırlıklı olarak **SQL sorguları** kullanarak çözmektir. Java tabanlı geçici veya hacky çözümlerden kaçınılmıştır.

Bu repository, **iki kişilik bir ekip tarafından geliştirilen proje için oluşturulmuş bireysel bir fork** olup, versiyon kontrolü ve kişisel geliştirme amacıyla kullanılmıştır.

---

## Sistem Özellikleri

- Konsol (terminal) tabanlı menü sistemi
- 3NF uyumlu MySQL veritabanı tasarımı
- JDBC ile veritabanı bağlantısı
- SQL odaklı veri yönetimi (DDL & DML)
- Kapsamlı hata yönetimi ve kullanıcı yönlendirmeleri

---

## Kullanıcı Rolleri

Sistem aşağıdaki kullanıcı rollerini destekler:

### Yönetici (Administrator)
- Oda ekleme, silme ve güncelleme
- Oda durumlarını yönetme
- Tüm rezervasyon ve housekeeping kayıtlarını görüntüleme
- Gelir raporları oluşturma
- Ödeme yapılmamış rezervasyonları iptal etme
- Yönetici hesapları yalnızca veritabanında tanımlıdır

### Resepsiyonist (Receptionist)
- Oda uygunluklarını görüntüleme
- Rezervasyon taleplerini yönetme
- Rezervasyonları onaylama veya reddetme
- Housekeeping görevlerini planlama

### Misafir (Guest)
- Uygun odalar için rezervasyon oluşturma
- Kendi rezervasyonlarını görüntüleme
- Onaylanan rezervasyonlar için check-in
- Ödeme tamamlandıktan sonra check-out işlemi

### Housekeeping
- Oda uygunluklarını görüntüleme (misafir bilgileri olmadan)
- Atanan temizlik planlarını görüntüleme
- Temizlik görevlerinin durumunu güncelleme

---

## Veritabanı Tasarımı

- Fonksiyonel bağımlılıklar dikkate alınarak tasarlanmıştır
- Tüm tablolar **3. Normal Form (3NF)** uyumludur
- Temel varlıklar:
  - Users, Roles
  - Rooms, Room Types
  - Bookings, Payments
  - Housekeeping Schedules
  - Employees
- Yabancı anahtarlar ile referans bütünlüğü sağlanmıştır
- Aynı odanın çakışan rezervasyonu veritabanı seviyesinde engellenmiştir
- Sadece temiz odalar rezerve edilebilir

---

## Proje Yapısı
```text
src/main/java/com/example/hotelmanagement
│
├── Entity
│ ├── Users, Roles, Guest, Employee, Administrator
│ ├── Room, Room_Type, Booking, Payments
│ ├── Housekeeping, HousekeepingSchedule
│ └── Reviews, Hotel
│
├── repository
│ ├── UsersRepository
│ ├── RoomRepository
│ ├── BookingRepository
│ ├── PaymentsRepository
│ ├── HousekeepingRepository
│ └── Other repository classes
│
├── services
│ ├── Booking management services
│ ├── Check-in / Check-out services
│ ├── Payment processing
│ ├── Administrator management services
│ └── Housekeeping scheduling and task management
│
├── ConsoleMenu.java
├── DatabaseConnection.java
└── Main.java
```

---

## Kullanılan Teknolojiler

- Java
- MySQL
- JDBC
- Gradle
- SQL (DDL & DML)

---

## Çalıştırma Adımları

1. `DDL.sql` dosyasını kullanarak veritabanını oluşturun
2. `DML.sql` dosyası ile örnek verileri ekleyin
3. `DatabaseConnection.java` dosyasında veritabanı bağlantı bilgilerini düzenleyin
4. `Main.java` sınıfını çalıştırın
5. Konsol menüsü üzerinden sistemi kullanın

---










