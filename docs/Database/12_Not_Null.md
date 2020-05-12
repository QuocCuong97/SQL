# Constraint `NOT NULL`
- Mặc định, một cột có thể giữ giá trị `NULL`
- **Constraint** `NOT NULL` bắt buộc cột không chấp nhận giá trị `NULL`, luôn luôn phải chứa giá trị. Điều này có nghĩa người dùng không thể thêm record mới, hoặc update record mà không nhập giá trị vào trường.
- **VD1:** Sử dụng `NOT NULL` khi tạo bảng :
    ```sql
    CREATE TABLE Persons (
        ID int NOT NULL,
        LastName varchar(255),
        FirstName varchar(255),
        Address varchar(255),
        City varchar(255)
    );
    ```
- **VD2 :** Thêm thuộc tính `NOT NULL` vào cột `ID` khi bảng đã tồn tại :
    ```sql
    ALTER TABLE Persons MODIFY ID int NOT NULL;
    ```
    <img src=https://i.imgur.com/lxSou95.png>