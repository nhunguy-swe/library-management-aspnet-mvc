# QLTV — Hệ thống Quản Lý Thư Viện (ASP.NET MVC)

<p>
  <img src="https://img.shields.io/badge/ASP.NET-MVC-512BD4" alt="ASP.NET MVC">
  <img src="https://img.shields.io/badge/C%23-.NET%20Framework-purple" alt="C#">
  <img src="https://img.shields.io/badge/Architecture-MVC-blue" alt="MVC">
</p>

**QLTV** (Quản Lý Thư Viện) là ứng dụng **web** quản lý và tra cứu thư viện, xây dựng bằng **ASP.NET MVC** (.NET Framework) theo mô hình MVC (Model – View – Controller). Ứng dụng cung cấp giao diện web hiển thị danh mục đầu sách kèm ảnh bìa, cho phép quản lý thông tin sách trong thư viện.

---

## Giới thiệu (About)

QLTV là một website quản lý thư viện, hiển thị danh mục sách với hình ảnh bìa trực quan theo nhiều thể loại (kinh tế, kế toán, ngôn ngữ, khoa học, thiếu nhi, kỹ năng sống...). Dự án được xây dựng để thực hành phát triển ứng dụng web trên nền tảng **ASP.NET MVC**, khai thác đầy đủ ba thành phần cốt lõi: **Controller** (xử lý request và điều hướng), **Model** (biểu diễn dữ liệu, ví dụ: Sách, Thể loại), và **View** (giao diện Razor hiển thị cho người dùng).

---

## Tính năng chính

- Hiển thị danh mục đầu sách kèm ảnh bìa, phân theo nhiều thể loại
- Tra cứu / xem thông tin chi tiết sách
- Giao diện web trực quan, có layout template riêng (`Template`, `ImagesLayout`)
- Quản lý dữ liệu sách qua Controller/Model theo chuẩn ASP.NET MVC

> Ghi chú: danh sách tính năng trên dựa theo cấu trúc thư mục hiện có. Nếu ứng dụng còn có thêm nghiệp vụ khác (đăng nhập, mượn/trả sách, quản lý độc giả...), bạn bổ sung thêm vào phần này cho đầy đủ.

---

## 🛠 Công nghệ sử dụng

| Thành phần | Công nghệ |
|---|---|
| Backend | C#, ASP.NET MVC (.NET Framework) |
| Frontend | Razor View, HTML/CSS/JavaScript (`Scripts`, `Content`, `assets`, `fonts`) |
| Kiến trúc | MVC (Model – View – Controller) |
| Quản lý gói | NuGet (`packages.config`) |
| IDE | Visual Studio |

---

## Cấu trúc dự án

```
QLTV/
├── App_Start/            # Cấu hình khởi tạo (RouteConfig, BundleConfig, FilterConfig...)
├── Controllers/           # Xử lý request, điều hướng nghiệp vụ
├── Models/                 # Các lớp dữ liệu (Sách, Thể loại...)
├── Views/                   # Giao diện Razor (.cshtml)
├── Content/                  # CSS và tài nguyên tĩnh
├── Scripts/                   # JavaScript
├── Images/                     # Ảnh bìa sách theo danh mục
├── ImagesLayout/                # Ảnh dùng cho giao diện/layout chung
├── Template/                      # Template giao diện
├── assets/, fonts/                 # Tài nguyên giao diện bổ sung
├── Properties/                      # Thông tin assembly
├── Global.asax / Global.asax.cs      # Cấu hình khởi động ứng dụng
├── Web.config / Web.Debug.config /    # Cấu hình ứng dụng theo môi trường
│   Web.Release.config
├── QLTV.csproj                          # File project Visual Studio
├── packages.config                       # Danh sách NuGet packages
└── favicon.ico
```

---

## Bắt đầu (Getting Started)

### Yêu cầu

- [Visual Studio](https://visualstudio.microsoft.com/) (2017 trở lên khuyến nghị)
- .NET Framework (phiên bản tương ứng với `QLTV.csproj`)
- IIS Express (đi kèm Visual Studio) để chạy web local

### Cài đặt

```bash
git clone https://github.com/nhunguy-swe/QLTV.git
cd QLTV
```

1. Mở file `QLTV.csproj` (hoặc solution chứa nó) bằng **Visual Studio**.
2. Visual Studio sẽ tự động khôi phục các gói NuGet theo `packages.config` (hoặc chạy **Restore NuGet Packages** thủ công nếu cần).
3. Nếu dự án có kết nối cơ sở dữ liệu, cập nhật **connection string** trong `Web.config` cho khớp với SQL Server/DB của bạn.

### Chạy ứng dụng

1. Đặt project làm **Startup Project** (nếu có nhiều project trong solution).
2. Nhấn **F5** hoặc **IIS Express ▶** trong Visual Studio để build và chạy.
3. Trình duyệt sẽ tự mở giao diện web tại địa chỉ local (ví dụ `http://localhost:xxxx`).

---

## Tác giả

- GitHub: [@nhunguy-swe](https://github.com/nhunguy-swe)

---

## Giấy phép

Dự án này được thực hiện cho mục đích học tập/đồ án cá nhân. Bạn có thể tham khảo, sử dụng lại code cho mục đích học tập.
