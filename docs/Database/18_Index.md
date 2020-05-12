# Lệnh `INDEX`
- Lệnh `INDEX` được sử dụng để tạo các chỉ mục (index) trong bảng .
- Sử dụng **index** để truy xuất dữ liaaju từ database sẽ nhanh hơn các cách khác .
- Người dùng không thể xem các **index** mà chúng chỉ được dùng để tăng tốc độ tìm kiếm / truy vấn .
### **CREATE INDEX**
- Tạo một **index** trong bảng, cho phép các giá trị trùng nhau 
    ```sql
    CREATE INDEX index_name ON table_name (column1, column2, ...);
    ```
- Tạo một **index** trong bảng, không cho phép các giá trị trùng nhau :
    ```sql
    CREATE UNIQUE INDEX index_name ON table_name (column1, column2, ...);
    ```
### **DROP INDEX**
- Được sử dụng để xóa một **index** trong bảng .
- Cú pháp :
    ```sql
    ALTER TABLE table_name DROP INDEX index_name;
    ```