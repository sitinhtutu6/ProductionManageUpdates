# 🏭 Production Manager

**Hệ thống Quản lý Sản xuất & Kinh doanh**

Production Manager là một ứng dụng web được xây dựng trên nền tảng **ASP.NET Core (MVC)** giúp doanh nghiệp quản lý quy trình từ đơn hàng, định mức nguyên vật liệu (BOM), kế hoạch sản xuất (MRP) đến kho bãi và tài chính.

## 🚀 Tính năng chính

* **Quản lý Đơn hàng (Sales Orders):** Theo dõi trạng thái, tiến độ sản xuất.
* **Mua hàng (Purchase Orders):** Quản lý nhập vật tư từ nhà cung cấp.
* **Kho hàng (Warehouse):** Nhập/Xuất, Kiểm kê, Cảnh báo tồn kho tối thiểu.
* **Sản xuất (Production):**
    * **BOM:** Quản lý định mức nguyên vật liệu đa cấp.
    * **MRP:** Tính toán nhu cầu vật tư tự động dựa trên đơn hàng.
    * **Kế hoạch:** Lên lịch sản xuất trực quan.
* **Tài chính:** Sổ thu chi (CashBook), Báo cáo doanh thu/lợi nhuận.
* **Hệ thống:** Phân quyền (RBAC), Thông báo (Notification), Đăng nhập bảo mật.

## ⚙️ Cài đặt & Chạy ứng dụng (Localhost)

### 1. Yêu cầu hệ thống
* [.NET SDK 8.0](https://dotnet.microsoft.com/download) trở lên.
* SQL Server (hoặc SQL Server Express/LocalDB).
* Visual Studio 2022 hoặc VS Code.
### 2. Cài đặt
- Bước 1: truy cập "https://github.com/sitinhtutu6/ProductionManageUpdates/releases" tải "ProductManagerWebsite.exe" bản mới nhất
- Bước 2: sau khi tải xong file ProductManagerWebsite.exe -> tiến hành run và cài đặt (next đến khi hoàn thành, trong quá trình cài đặt ứng dụng cần một số lib hỗ trợ hãy cài đặt chúng nếu hiện lên)
- Bước 3: Run app sau khi cài đặt xong, nếu báo thiếu thư viện -> nhấn mũi tên để thấy link tải lib về và cài đặt
- Bước 4: Config như hình: <img width="925" height="981" alt="config" src="https://github.com/user-attachments/assets/413da429-195d-4a73-9607-dbe3000bee8b" />
- Bước 5: Lưu cấu hình và Start LAN, sau đó nhấn tìm web (nếu muốn public internet hãy nhấn Public website, limite: <50 người truy cập cùng lúc)
- Bước 6: Đăng ký tài khoản và confirm Email (Admin) -> restart lại server (start LAN) để cập nhật email Admin

### 3. Cách để lấy App password: 
- 1. truy cập: [Google Account Security.](https://myaccount.google.com/u/1/security)
- 2. Bật Xác thực 2 bước (2-Step Verification) nếu chưa bật.
- 3. Tìm mục Mật khẩu ứng dụng (App Passwords) (hoặc gõ vào ô tìm kiếm).
- 4. Tạo tên ứng dụng mới (VD: ProductionApp) -> Bấm Create.
- 5. Google sẽ cấp một chuỗi 16 ký tự. Copy chuỗi này -> Paste vào ô App password.
- 6. Lưu cấu hình

### 4. Cách lấy Telegram Bot Token (Thông báo qua Chat)
- 1. Mở Telegram, tìm kiếm user @BotFather.
- 2. Chat lệnh: /newbot.
- 3. Đặt tên hiển thị (VD: Production Notify) và username (kết thúc bằng bot, VD: MyProdBot).
- 4. BotFather sẽ gửi cho bạn HTTP API Token. Copy token này.
- 5. Để lấy ChatId (người nhận tin):
    + Tạo phòng chat (new channel) và Add bot vừa tạo vào, sau đó truy cập vào phòng chat
    + Link web có dạng: https://web.telegram.org/k/#-5115188192
    + Chat ID là: -5115188192 hãy copy và paste vào Tele Chat ID
