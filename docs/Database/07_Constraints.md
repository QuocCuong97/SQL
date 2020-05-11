# Constraints
- **Constraints** ( hay ***ràng buộc*** ) dùng để chỉ ra rule cho dữ liệu trong bảng .
- Các **constraints** được sử dụng để loại dữ liệu đi vào bảng . Điều này đảm bảo tính chính xác và độ tin cậy của dữ liệu trong bảng . Nếu có action nào đi ngược với **constraints**, hành động đó sẽ bị hủy bỏ .
- Các **constraints** có thể ở mức cột hoặc mức bảng . Các **constraints** mức cột áp dụng cho một cột còn **constraints** mức bảng áp dụng cho toàn bộ bảng .
### **Tạo constraints**
- **Constraints** có thể được chỉ định khi tạo bảng qua lệnh `CREATE TABLE` hoặc cũng có thể sau khi bảng được tạo bằng lệnh `ALTER TABLE` :
    ```sql
    CREATE TABLE table_name (column1 datatype constraint, column2 datatype constraint, column3 datatype constraint, .... );
    ```
### **Một số constraint thường dùng trong SQL**
- `NOT NULL` - Đảm bảo rằng 1 cột không chứa giá trị `NULL`
- `UNIQUE` - Đảm bảo tất cả các giá trị trong cột là khác nhau 
- `PRIMARY KEY` - Là cột kết hợp `NOT NULL` và `UNIQUE` . Mỗi giá trị trong cột xác định chính xác 1 hàng trong bảng .
- `FOREIGN KEY` - Xác định 1 hàng/bản ghi trên bảng khác 
- `CHECK` - Đảm bảo rằng tất cả các dữ liệu trong 1 cột thỏa mãn 1 điều kiện cụ thể 
- `DEFAULT` - Đặt giá trị mặc định cho cột khi khi không có giá trị được khai báo
- `INDEX` - Sử dụng để tạo và lấy dữ liệu từ database rất nhanh .

