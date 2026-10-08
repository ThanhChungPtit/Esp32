# 🚗 Hệ Thống Giám Sát Nhà Để Xe (ESP32 + RFID)

Dự án xây dựng hệ thống quản lý và giám sát bãi đỗ xe thông minh ứng dụng vi điều khiển **ESP32** kết hợp với công nghệ định danh **RFID**, hỗ trợ điều khiển và theo dõi trạng thái qua Web/Server.

---

## 📌 Tính Năng Chính

* 🎴 **Quản lý vào/ra bằng RFID:** Tự động quẹt thẻ định danh xe và người dùng.
* 🚪 **Điều khiển đóng/mở barie:** Tự động điều khiển động cơ Servo/Barie khi thẻ hợp lệ.
* 📊 **Giám sát thời gian thực:** Gửi dữ liệu trạng thái chỗ đỗ xe, nhật ký vào/ra lên Web Server.
* 🚨 **Cảnh báo an toàn:** Phát hiện xe không hợp lệ hoặc sự cố tại nhà xe.

---

## 🛠️ Cấu Trúc Dự Án (ESP-IDF)

```text
Hethonggiamsatnhadexe/
├── components/          # Các thư viện & driver ngoại vi (RFID, LCD/TFT, Wi-Fi,...)
├── main/                # Mã nguồn chính dự án (main.c, ứng dụng điều khiển)
├── build/               # Thư mục biên dịch của ESP-IDF
├── CMakeLists.txt       # Cấu hình biên dịch CMake
└── sdkconfig            # Cấu hình phần cứng & tính năng ESP32
