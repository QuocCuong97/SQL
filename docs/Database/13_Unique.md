# Constraint `UNIQUE`
- **Constraint** `UNIQUE` đảm bảo rằng tất cả các giá trị trong cột là khác nhau .
- Cả **constraint** `UNIQUE` và `PRIMARY KEY` đều đảm bảo sự duy nhất của các giá trị trong cột .
- **Constraint** `PRIMARY KEY` tự động bao gồm **constraint** `UNIQUE`
- Có thể có nhiều **constraint** `UNIQUE` trên mỗi bảng, nhưng chỉ có một **constraint** `PRIMARY KEY` trong bảng .
- **VD1:** Sử dụng `UNIQUE` khi tạo bảng :
    ```sql
    CREATE TABLE Persons (
        ID int NOT NULL UNIQUE,
        LastName varchar(255),
        FirstName varchar(255),
        Address varchar(255),
        City varchar(255)
    );
    ```
- **VD2 :** Thêm thuộc tính `UNIQUE` vào cột `ID` khi bảng đã tồn tại :
    ```sql
    ALTER TABLE Persons MODIFY ID int UNIQUE;
    ```
    <img src=https://i.imgur.com/umsTMi8.png>

- **VD3 :** Xóa thuộc tính `UNIQUE` đã tồn tại trên cột `ID` :
    ```sql
    ALTER TABLE Persons DROP INDEX;
    ```