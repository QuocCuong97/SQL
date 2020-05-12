# Lệnh `ALTER TABLE`
- Lệnh `ALTER TABLE` được sử dụng để thêm, xóa hoặc sửa cột trong bảng đã có sẵn .
- Lệnh `ALTER TABLE` cũng được sử dụng để thêm hoặc xóa các ràng buộc khác nhau trong bảng hiện có .
### **Thêm cột**
- Cú pháp :
    ```sql
    ALTER TABLE table_name ADD column_name datatype;
    ```
- **VD :** Thêm cột `Email` :
    ```sql
    ALTER TABLE Persons ADD Email varchar(255);
    ```
    <img src=https://i.imgur.com/SjqtVOe.png>
### **Xóa cột**
- Cú pháp :
    ```sql
    ALTER TABLE table_name DROP COLUMN column_name;
    ```
> Một số loại database không cho phép xóa cột!
- **VD :** Xóa cột `Email` :
    ```sql
    ALTER TABLE Persons DROP COLUMN Email;
    ```
    <img src=https://i.imgur.com/tnYfh3C.png>
### **Sửa cột (thay đổi tên và kiểu dữ liệu)**
- Cú pháp :
    ```sql
    ALTER TABLE table_name CHANGE old_column_name new_column_name datatype;
    ```
- **VD :** Sửa cột `PersonID` thành `ID` với kiểu dữ liệu `int(5)`:
    ```sql
    ALTER TABLE Persons CHANGE PersonID ID int(5);
    ```
    <img src=https://i.imgur.com/PGMXJIr.png>