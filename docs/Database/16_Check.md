# Constraint `CHECK`
- **Constraint** `CHECK` được sử dụng để giới hạn day giá trị có thể được đặt trong cột .
- Nếu định nghĩa một **constraint** `CHECK` trên một cột đơn lẻ, nó sẽ chỉ cho phép những giá trị chính xác được lưu trong cột .
- Nếu định nghĩa một **constraint** `CHECK` trên một bảng, nó sẽ giới hạn giá trị trên cột dựa trên các cột khác ở cùng một hàng .
- **VD1:** Sử dụng `CHECK` khi tạo bảng :
    ```sql
    CREATE TABLE Persons (
        ID int NOT NULL PRIMARY KEY,
        LastName varchar(255),
        FirstName varchar(255),
        Address varchar(255),
        City varchar(255)
        CHECK (ID>=18)
    );
    ```
- **VD2 :** Thêm thuộc tính `PRIMARY KEY` vào cột `ID` khi bảng đã tồn tại :
    ```sql
    ALTER TABLE Persons ADD CHECK (ID>=18);
    ```
    <img src=https://i.imgur.com/yyCoMEi.png>

- **VD3 :** Xóa thuộc tính `PRIMARY KEY` đã tồn tại của bảng :
    ```sql
    ALTER TABLE Persons DROP CHECK;
    ```
- **VD4 :** Đặt tên cho `CHECK` :
    ```sql
    CREATE TABLE Persons (
        ID int NOT NULL PRIMARY KEY,
        LastName varchar(255),
        FirstName varchar(255),
        Address varchar(255),
        City varchar(255)
        CONSTRAINT CHK_Person CHECK (ID>=18 AND City='Sandnes')
    );
    ```
    => Xóa `CHECK` theo tên :
    ```sql
    ALTER TABLE Persons DROP CHECK CHK_Person;