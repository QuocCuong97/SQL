# Các kiểu dữ liệu trong SQL
## **Kiểu dữ liệu string**

| Kiểu dữ liệu | Mô tả |
|--------------|-------|
| `CHAR(size)` | Đoạn string có chiều dài cố định (có thể chứa chữ cái, số và ký tự đặc biệt). Tham số `size` xác định chiều dài cố định của cột (số kí tự tối đa) - có thể từ `0` -> `255`. Mặc định là `1` . | 
| `VARCHAR(size)` | Đoạn string có chiều dài thay đổi (có thể chứa chữ cái, số và ký tự đặc biệt). Tham số `size` xác định chiều dài tối đa của cột (số kí tự tối đa) - có thể từ `0` -> `65535`. |
| `BINARY(size)` | Giống với `CHAR()`, nhưng lưu trữ các ký tự nhị phân. Tham số `size` xác định chiều dài của cột theo `bytes`. Mặc định là `1`. |
| `VARBINARY(size)` | Giống với `VARCHAR()`, nhưng lưu trữ các ký tự nhị phân. Tham số `size` xác định chiều dài của cột theo `bytes`. |
| `TINYBLOB` | Dành cho BLOBs (Binary Large OBjects). Chiều dài tối đa `255 Bytes` |
| `TINYTEXT` | Giữ một chuỗi với độ dài tối đa `255` ký tự |
| `TEXT(size)` | Giữ một chuỗi chuỗi có độ dài tối đa `65535 Bytes` |
| `BLOB(size)` | |
| `MEDIUMTEXT` | |
| `MEDIUMBLOB` | |
| `LONGTEXT` | |
| `LONGBLOB` | |
| `ENUM(val1, val2, val3, ...)` | |
| `SET(val1, val2, val3, ...)` | |
Equal to CHAR(), but stores binary byte strings. The size parameter specifies the column length in bytes. Default is 1
## **Kiểu dữ liệu number**

| Kiểu dữ liệu | Mô tả |
|--------------|-------|
| `BIT(size)` | |
| `TINYINT(size)` | |
| `BOOL` | |
| `BOOLEAN` | |
| `SMALLINT(size)` | |
| `MEDIUMINT(size)` | |
| `INT(size)` |  |
| `INTEGER(size)` | Số nguyên bình thường. Khoảng giới hạn từ `-2147483648` đến `2147483647`. Tham số `size` định nghĩa số chữ số hiển thị tối đa (tối đa `255`) |
| `BIGINT(size)` |  |
| `FLOAT(size, d)` | Số thập phân. Tham số `size` định nghĩa số chữ số sẽ hiển thị tối đa. Tham số `d` địng nghĩa số chữ số đằng sau dấu phẩy |
| `FLOAT(p)` | |
| `DOUBLE(size, d)` | |
| `DOUBLE PRECISION(size, d)` | |
| `DECIMAL(size, d)` | |
| `DEC(size, d)` | |
	A floating point number. The total number of digits is specified in size. The number of digits after the decimal point is specified in the d parameter. This syntax is deprecated in MySQL 8.0.17, and it will be removed in future MySQL versions
## **Kiểu dữ liệu date and time**

| Kiểu dữ liệu | Mô tả |
|--------------|-------|
| `DATE` | Ngày. Định dạng `YYYY-MM-DD`. Hỗ trợ từ `1000-01-01` đến `9999-12-31` |
| `DATETIME(fsp)` | Ngày và giờ. Định dạng `YYYY-MM-DD hh:mm:ss`. Hỗ trợ từ `1000-01-01 00:00:00` đến `9999-12-31 23:59:59` . Thêm thuộc tính `DEFAULT` và `ON UPDATE` khi định nghĩa cột để tự động khởi tạo và update thời gian hiện giờ |
| `TIMESTAMP(fsp)` | Mốc thời gian. Timestamp lưu trữ số giây bắt đầu từ `'1970-01-01 00:00:00' UTC` đến thời điểm hiện tại. Định dạng `YYYY-MM-DD hh:mm:ss`. Hỗ trợ từ `'1970-01-01 00:00:01' UTC` đến `'2038-01-09 03:14:07' UTC` . Thêm thuộc tính `DEFAULT CURRENT_TIMESTAMP` và `DEFAULT CURRENT_TIMESTAMP` khi định nghĩa cột để tự động khởi tạo và update thời gian hiện giờ |
| `TIME(fsp)` | Thời gian. Định dạng `hh:mm:ss`. Hỗ trợ từ `-838:59:59` đến `838:59:59` |
| `YEAR` | Năm ở định dạng 4 ký tự. Giá trị cho phép : `1901 - 2155` và `0000` . **MySQL** `8.0` không hỗ trợ dạng 2 ký tự |
