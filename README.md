Dự án đọc và hiển thị thời gian từ đồng hồ thời gian thực DS1307 lên màn hình LCD thông qua giao tiếp I2C.
 
Các thư viện: Bao gồm các tệp tiêu đề cần thiết như main.h, i2c-lcd.h, và stdio.h.

Định nghĩa địa chỉ I2C của DS1307: #define DS1307_ADDR (0x68 << 1)

Cấu trúc thời gian DS1307: Được định nghĩa với các thành phần như giây, phút, giờ, ngày trong tuần, ngày, tháng và năm.

I2C_HandleTypeDef hi2c1: Cấu trúc điều khiển I2C.

Biến thời gian time: Khởi tạo với giá trị cụ thể.

Buffer: char buf0[25]; và char buf1[25]; dùng để lưu chuỗi ký tự hiển thị trên LCD.

B2D: Chuyển đổi từ BCD (Binary-Coded Decimal) sang thập phân.

D2B: Chuyển đổi từ thập phân sang BCD.

SET_TIME: Thiết lập thời gian cho DS1307 bằng cách chuyển đổi giá trị từ thập phân sang BCD và ghi vào DS1307 qua I2C.

GET_TIME: Đọc thời gian từ DS1307 và chuyển đổi từ BCD sang thập phân.

