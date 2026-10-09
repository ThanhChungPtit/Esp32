# 🚀 Tổng Hợp Các Dự Án ESP32 & Hệ Thống Nhúng (Embedded Projects)

Repository này lưu trữ các dự án lập trình ứng dụng vi điều khiển **ESP32**, xây dựng hệ thống đỗ xe thông minh, mô-đun giám sát qua Web Server, MQTT và quản lý phần cứng bằng framework **ESP-IDF**.

---

## 📂 Danh Sách Các Dự Án

### 1. 🏢 `Hethonggiamsatnhadexe/` - Hệ Thống Giám Sát Nhà Để Xe (ESP-IDF + Web Server)
* **Mô tả:** Hệ thống quản lý bãi đỗ xe tự động theo thời gian thực sử dụng ESP32 kết hợp định danh RFID RC522.
* **Tính năng chính:**
  * 🎴 **Định danh RFID:** Xác thực thẻ xe khi vào/ra bãi.
  * 🌐 **Web Server & MQTT:** Tích hợp giao diện Web Dashboard giám sát số lượng chỗ đỗ, điều khiển mở barie từ xa và đồng bộ dữ liệu.
  * 🌡️ **Cảm biến môi trường:** Đọc cảm biến nhiệt độ, độ ẩm (DHT) và cảm biến hồng ngoại (IR) phát hiện xe.
  * ⚙️ **Mô-đun hóa (Components):** Cấu trúc thư viện tách biệt gồm `DHT`, `LCD`, `RFID`, `SERVO`, `SPI`, `my_mqtt`, `my_wifi`.

### 2. 🌐 `BaiDoXe-main/` - Giao Diện Web Giám Sát Bãi Đỗ Xe
* **Mô tả:** Mã nguồn phần giao diện Web Server phục vụ việc hiển thị trực quan nhật ký xe vào/ra, trạng thái các vị trí đỗ và điều khiển hệ thống.

---

## 🛠️ Công Cụ & Môi Trường Phát Triển

* **Vi điều khiển:** ESP32 DevKit V1 / ESP32-WROOM
* **Framework / IDE:** ESP-IDF (v5.x), VS Code, Git
* **Giao thức:** Wi-Fi, MQTT, HTTP Web Server, SPI, I2C, UART, PWM

---

## 👨‍💻 Tác Giả

* **Nguyễn Thành Chung** (`ThanhChungPtit`)
* **Trường:** Học viện Công nghệ Bưu chính Viễn thông (PTIT)
