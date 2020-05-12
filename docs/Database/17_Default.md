# Constraint `DEFAULT`
- **Constraint** `DEFAULT` được sử dụng để cung cấp giá rtij mặc định cho cột
- Giá trị **default** sẽ được thêm vào các record mới nếu không có giá trị nào được khai báo .
- **VD1:** Sử dụng `DEFAULT` khi tạo bảng :
    ```sql
    CREATE TABLE Persons (
        ID int NOT NULL PRIMARY KEY,
        LastName varchar(255),
        FirstName varchar(255),
        Address varchar(255),
        City varchar(255) DEFAULT 'Sandnes'
    );
    ```
- **VD2 :** Thêm thuộc tính `PRIMARY KEY` vào cột `ID` khi bảng đã tồn tại :
    ```sql
    ALTER TABLE Persons ALTER City SET DEFAULT 'Sandnes';
    ```
    <img src=https://i.imgur.com/yyCoMEi.png>

- **VD3 :** Xóa thuộc tính `PRIMARY KEY` đã tồn tại của bảng :
    ```sql
    ALTER TABLE Persons DROP PRIMARY KEY;
    ```
    <img src=https://i.imgur.com/npebBkt.png>