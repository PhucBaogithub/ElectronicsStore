# Electronics Store

Một ứng dụng web bán hàng điện tử được xây dựng với ASP.NET Core và Entity Framework.

## Tính năng

- 🛍️ Hiển thị danh sách sản phẩm
- 🛒 Giỏ hàng
- 👤 Đăng ký/Đăng nhập người dùng
- 👑 Quản trị admin
- 📱 Quản lý danh mục sản phẩm
- 💳 Quản lý đơn hàng
- 🔐 Xác thực JWT

## Công nghệ sử dụng

- ASP.NET Core 9.0
- Entity Framework Core
- SQLite Database
- JWT Authentication
- Bootstrap CSS
- BCrypt cho mã hóa mật khẩu

## Cấu trúc project

```
ElectronicsStore/
├── Controllers/        # Các controller xử lý request
├── Models/            # Các model và DTO
├── Data/              # DbContext và cấu hình database
├── Views/             # Razor views
├── wwwroot/           # Static files (CSS, JS, Images)
└── Migrations/        # Entity Framework migrations
```

## Cài đặt và chạy

1. Clone repository:
```bash
git clone <repository-url>
cd ElectronicsStore
```

2. Restore packages:
```bash
dotnet restore
```

3. Update database:
```bash
dotnet ef database update
```

4. Chạy ứng dụng:
```bash
dotnet run
```

5. Mở trình duyệt và truy cập: `https://localhost:5001`

## API Endpoints

### Authentication
- `POST /api/auth/register` - Đăng ký tài khoản
- `POST /api/auth/login` - Đăng nhập

### Products
- `GET /api/products` - Lấy danh sách sản phẩm
- `GET /api/products/{id}` - Lấy chi tiết sản phẩm

### Cart
- `GET /api/cart` - Lấy giỏ hàng
- `POST /api/cart/add` - Thêm sản phẩm vào giỏ
- `PUT /api/cart/update` - Cập nhật số lượng
- `DELETE /api/cart/remove/{id}` - Xóa sản phẩm khỏi giỏ

### Admin (Yêu cầu quyền admin)
- `GET /api/admin/users` - Quản lý người dùng
- `GET /api/admin/orders` - Quản lý đơn hàng
- `POST /api/admin/products` - Tạo sản phẩm mới
- `PUT /api/admin/products/{id}` - Cập nhật sản phẩm
- `DELETE /api/admin/products/{id}` - Xóa sản phẩm

## Tác giả

Huỳnh Phúc Bảo

## License

MIT License 
