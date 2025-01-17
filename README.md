# 🌐 Excersie4: Web Service với MongoDB

## 📝 Mô tả dự án

Dự án này sử dụng **ASP.NET Core** để xây dựng một dịch vụ web RESTful kết nối với cơ sở dữ liệu **MongoDB**. Dịch vụ này cung cấp các API để quản lý dữ liệu, bao gồm các chức năng cơ bản như tạo, đọc, cập nhật và xóa dữ liệu (CRUD).

## 📂 Cấu trúc dự án

### Thư mục chính:
- **Controllers**: Chứa các API controller để xử lý các yêu cầu từ client.
- **Models**: Định nghĩa các lớp mô hình (model) để ánh xạ dữ liệu.
- **Services**: Chứa các lớp xử lý nghiệp vụ, bao gồm truy xuất và tương tác với cơ sở dữ liệu MongoDB.
- **Properties**: Cấu hình ứng dụng, bao gồm tệp `launchSettings.json`.

## 🚀 Hướng dẫn cài đặt và chạy

1. **Clone repository**:

   ```bash
   git clone https://github.com/soa-ueh-thanhlam/Excersie4.git
   ```

2. **Cài đặt các thư viện cần thiết**:

   Điều hướng vào thư mục dự án và chạy lệnh sau để cài đặt các gói NuGet:

   ```bash
   dotnet restore
   ```

3. **Cấu hình MongoDB**:

   - Mở tệp `appsettings.json` và chỉnh sửa thông tin kết nối MongoDB:

     ```json
     {
       "MongoDB": {
         "ConnectionString": "mongodb://localhost:27017",
         "DatabaseName": "YourDatabaseName"
       }
     }
     ```

   - Đảm bảo rằng MongoDB đã được cài đặt và đang chạy trên máy chủ của bạn.

4. **Chạy ứng dụng**:

   ```bash
   dotnet run
   ```

5. **Kiểm tra API**:

   Mở trình duyệt và truy cập tài liệu Swagger tại:

   ```
   http://localhost:<port>/swagger
   ```

## ⚙️ Chức năng chính

### Các API được cung cấp:

| HTTP Method | Endpoint            | Mô tả                              |
|-------------|---------------------|-------------------------------------|
| GET         | `/items`            | Lấy danh sách tất cả các mục       |
| GET         | `/items/{id}`       | Lấy thông tin chi tiết theo ID     |
| POST        | `/items`            | Tạo một mục mới                   |
| PUT         | `/items/{id}`       | Cập nhật một mục theo ID          |
| DELETE      | `/items/{id}`       | Xóa một mục theo ID               |

## 🛠️ Công nghệ sử dụng

- **ASP.NET Core**: Framework chính để xây dựng dịch vụ web.
- **MongoDB.Driver**: Thư viện để kết nối và thao tác với MongoDB.
- **Swagger**: Công cụ tự động tạo tài liệu API và kiểm thử các endpoint.

## 🛡️ Bảo mật

- Sử dụng kết nối an toàn với MongoDB (nếu chạy trên môi trường sản xuất).
- Cấu hình tường lửa để bảo vệ cơ sở dữ liệu khỏi truy cập trái phép.

## ✍️ Tác giả

- **Đoàn Thanh Lâm**: [GitHub Profile](https://github.com/thanhlamcode)

## 📚 Tài liệu tham khảo

- [Microsoft Docs: ASP.NET Core Web API](https://learn.microsoft.com/en-us/aspnet/core/web-api/)
- [MongoDB Driver Documentation](https://www.mongodb.com/docs/drivers/csharp/)
- [Hướng dẫn cài đặt MongoDB](https://www.mongodb.com/docs/manual/installation/)
