# 🛒 Modern E-Ticaret Web Uygulaması | ASP.NET Core MVC & MongoDB

Bu proje M&Y Akademi Danışmanlık bünyesinde Murat Yücedağ eğitmenliğinde, **MongoDB** veritabanı ve **ASP.NET Core MVC** mimarisi ile geliştirilmiş,  Kullanıcılar ürünleri görüntüleyebilir, slider bileşenleri aracılığıyla kampanyaları takip edebilir ve e-posta aboneliği ile indirim kuponlarına ulaşabilirler. Yönetim paneli sayesinde içerikler kolayca kontrol edilebilir.

---

## ✨ Öne Çıkan Özellikler

- 📦 NoSQL tabanlı MongoDB veri yapısı
- 🛍️ Ürün, kategori ve kampanya (slider) yönetimi
- 💌 E-posta abonelik sistemi (otomatik %20 indirim kuponu)
- 🧩 Reusable Component & Partial View kullanımı
- 🔄 Asenkron veri işlemleri (Async/Await)
- 🧠 DTO (Data Transfer Object) ve servis katmanı mimarisi
- 🔐 Admin panel üzerinden içerik yönetimi

---

## 🧩 Mimari Yapı

### 🔹 Katmanlar

- **Controllers**: HTTP isteklerini işler, servisleri çağırır.
- **Services**: Veritabanı işlemlerini kapsüller.
- **DTOs**: Veri transferini sağlar (Model ↔ View).
- **Views**: Razor Pages ile geliştirilen kullanıcı arayüzü.
- **Partials/Components**: Yeniden kullanılabilir HTML parçaları (örneğin: slider, ürün kartları).

---

## 🗃️ MongoDB Veri Modeli

Projede kullanılan ana koleksiyonlar:

- **Products**  
  `ProductId`, `ProductName`, `Price`, `Description`, `CategoryId`, `List<ProductImage>`

- **ProductImages**  
  `ProductImageId`, `ProductImageUrl`

- **Categories**  
  `CategoryId`, `CategoryName`

- **Sliders**  
  `SliderId`, `Title`, `ImageUrl`

İlişkiler, referans ID üzerinden sağlanmıştır (örneğin: bir ürün `CategoryId` alanı ile kategoriye bağlanır).

---

## 📬 E-Posta Aboneliği ve İndirim Kuponu

Kullanıcılar, e-posta adreslerini bırakarak sistem tarafından otomatik oluşturulan **%20 indirim kodu** alırlar.

- Kodlar 8 karakter uzunluğunda rastgele alfanümerik şekilde üretilir ve kullanıcıya bununla ilgili mail gider. İlgili maile tanımlandığı bildirilir.
- Gönderimler **Gmail SMTP** üzerinden yapılır.
- Güvenlik için uygulama şifresi kullanılır.

## 🧪 Kullanılan Teknolojiler

| Teknoloji               | Açıklama                                                                 |
|-------------------------|--------------------------------------------------------------------------|
| **ASP.NET Core MVC**    | Web uygulama geliştirme çatısı                                           |
| **MongoDB (NoSQL)**     | Esnek veri yapısı sunan belge tabanlı NoSQL veritabanı                   |
| **SMTP (Gmail App PW)** | Gmail SMTP sunucusu üzerinden güvenli e-posta gönderimi                  |
| **Bootstrap 5**         | Duyarlı (responsive) ve modern kullanıcı arayüzü için CSS framework'ü   |
| **C# 10**               | Modern C# sürümü ile güçlü backend geliştirme                            |
| **JavaScript**          | Dinamik işlemler ve veri alışverişi (AJAX - Fetch API ile)               |
| **LINQ**                | Koleksiyonlar ve veriler üzerinde güçlü sorgulama özelliği               |
| **Async / Await**       | Asenkron veri işlemleri ve performanslı API kullanımı                    |
| **DTO Pattern**         | Katmanlar arası veri aktarımı                            


# 📸 Proje Görselleri

![ImageAlt](https://github.com/SemihSanli/ShoppingNightMongo/blob/065b27944a9b7e04a24e0c990e20947d64c1f496/Images/Ekran%20g%C3%B6r%C3%BCnt%C3%BCs%C3%BC%202025-05-23%20234757.png)
![ImageAlt](https://github.com/SemihSanli/ShoppingNightMongo/blob/065b27944a9b7e04a24e0c990e20947d64c1f496/Images/Ekran%20g%C3%B6r%C3%BCnt%C3%BCs%C3%BC%202025-05-23%20234811.png)
![ImageAlt](https://github.com/SemihSanli/ShoppingNightMongo/blob/065b27944a9b7e04a24e0c990e20947d64c1f496/Images/Ekran%20g%C3%B6r%C3%BCnt%C3%BCs%C3%BC%202025-05-23%20131314.png)
![ImageAlt](https://github.com/SemihSanli/ShoppingNightMongo/blob/065b27944a9b7e04a24e0c990e20947d64c1f496/Images/Ekran%20g%C3%B6r%C3%BCnt%C3%BCs%C3%BC%202025-05-23%20234822.png)
![ImageAlt](https://github.com/SemihSanli/ShoppingNightMongo/blob/065b27944a9b7e04a24e0c990e20947d64c1f496/Images/Ekran%20g%C3%B6r%C3%BCnt%C3%BCs%C3%BC%202025-05-23%20235449.png)
![ImageAlt](https://github.com/SemihSanli/ShoppingNightMongo/blob/065b27944a9b7e04a24e0c990e20947d64c1f496/Images/Ekran%20g%C3%B6r%C3%BCnt%C3%BCs%C3%BC%202025-05-23%20235459.png)
![ImageAlt](https://github.com/SemihSanli/ShoppingNightMongo/blob/065b27944a9b7e04a24e0c990e20947d64c1f496/Images/Ekran%20g%C3%B6r%C3%BCnt%C3%BCs%C3%BC%202025-05-23%20235748.png)
![ImageAlt](https://github.com/SemihSanli/ShoppingNightMongo/blob/065b27944a9b7e04a24e0c990e20947d64c1f496/Images/Ekran%20g%C3%B6r%C3%BCnt%C3%BCs%C3%BC%202025-05-24%20000156.png)
![ImageAlt](https://github.com/SemihSanli/ShoppingNightMongo/blob/065b27944a9b7e04a24e0c990e20947d64c1f496/Images/WhatsApp%20G%C3%B6rsel%202025-05-23%20saat%2011.16.32_e37bf24b.jpg)
