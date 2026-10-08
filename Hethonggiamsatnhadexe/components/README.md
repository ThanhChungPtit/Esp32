# 📦 Thư Viện & Driver Dự Án (Components)

Thư mục này chứa toàn bộ các mô-đun thư viện và driver ngoại vi được thiết kế cho dự án Hệ thống giám sát nhà đỗ xe trên nền tảng **ESP-IDF**.

---

## 📂 Chi Tiết Từng Component

| Component | Chức Năng Chính |
| :--- | :--- |
| **`DHT`** | Driver giao tiếp và đọc dữ liệu nhiệt độ, độ ẩm từ cảm biến DHT11 / DHT22. |
| **`LCD`** | Thư viện điều khiển màn hình LCD (1602/2004) qua giao tiếp I2C để hiển thị thông tin hướng dẫn, trạng thái xe vào/ra. |
| **`RFID`** | Driver giao tiếp với mô-đun đọc thẻ RFID RC522 (13.56 MHz) qua giao thức SPI để định danh thẻ xe. |
| **`SERVO`** | Điều khiển động cơ Servo PWM dùng làm cần barie tự động đóng/mở cổng nhà xe. |
| **`SPI`** | Thư viện giao tiếp chuẩn SPI cơ sở (dùng chung cho RFID hoặc màn hình TFT). |
| **`my_mqtt`** | Mô-đun kết nối và giao tiếp giao thức MQTT, gửi dữ liệu lịch sử xe vào/ra và nhận lệnh điều khiển từ server/broker. |
| **`my_wifi`** | Quản lý kết nối Wi-Fi cho ESP32 (kết nối Station, tự động thử lại khi mất mạng và đồng bộ thời gian NTP). |

---

## 🛠️ Cách Sử Dụng Trong Dự Án (ESP-IDF)

Các component này đã được cấu hình tương thích với hệ thống build **CMake** của ESP-IDF. Khi biên dịch ứng dụng chính tại thư mục `main`, các driver trên sẽ tự động được liên kết (link) vào dự án.

```cmake
# Ví dụ cấu hình trong CMakeLists.txt tại main/
idf_component_register(SRCS "main.c"
                       INCLUDE_DIRS "."
                       REQUIRES DHT LCD RFID SERVO SPI my_mqtt my_wifi)
