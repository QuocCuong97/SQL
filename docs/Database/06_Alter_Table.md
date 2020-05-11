# Lệnh `ALTER TABLE`
- Lệnh `ALTER TABLE` được sử dụng để thêm, xóa hoặc sửa cột trong bảng đã có sẵn .
- Lệnh `ALTER TABLE` cũng được sử dụng để thêm hoặc xóa các ràng buộc khác nhau trong bảng hiện có .
### **Thêm cột**
- Cú pháp :
    ```sql
    ALTER TABLE table_name ADD column_name datatype;
    ```
### **Xóa cột**
- Cú pháp :
    ```sql
    ALTER TABLE table_name DROP COLUMN column_name;
    ```
> Một số loại database không cho phép xóa cột!
### **Sửa cột (thay đổi kiểu dữ liệu)**
- Cú pháp :
    ```sql
    ALTER TABLE table_name MODIFY COLUMN column_name datatype;
    ```
