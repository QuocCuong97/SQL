# Constraint `PRIMARY KEY`
- **Constraint** `PRIMARY KEY` cho phép nhận dạng từng record trong bảng một cách duy nhất .
- Primary key phải chứa các giá trị UNIQUE (duy nhất), và không thể chứa giá trị `NULL`
- Một bảng chỉ có thể có một **primary key** .
- Trong một bảng, **primary** có thể bao gồm 1 hoặc nhiều cột .
- **VD1:** Sử dụng `PRIMARY KEY` khi tạo bảng :
    ```sql
    CREATE TABLE Persons (
        ID int NOT NULL PRIMARY KEY,
        LastName varchar(255),
        FirstName varchar(255),
        Address varchar(255),
        City varchar(255)
    );
    ```
- **VD2 :** Thêm thuộc tính `PRIMARY KEY` vào cột `ID` khi bảng đã tồn tại :
    ```sql
    ALTER TABLE Persons ADD PRIMARY KEY (ID);
    ```
    <img src=https://i.imgur.com/yyCoMEi.png>

- **VD3 :** Xóa thuộc tính `PRIMARY KEY` đã tồn tại của bảng :
    ```sql
    ALTER TABLE Persons DROP PRIMARY KEY;
    ```
