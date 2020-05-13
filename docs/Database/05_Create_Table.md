# Lệnh `CREATE TABLE`
- Lệnh `CREATE TABLE` được sử dụng để tạo bảng mới trong database .
- Cú pháp :
    ```sql
    CREATE TABLE table_name (column1 datatype, column2 datatype, column3 datatype, ....);
    ```
    - Trong đó :
        - Tham số `column*` chỉ định tên các cột của bảng
        - Tham số `datatype` chỉ định kiểu dữ liệu của các cột (VD: `varchar`, `integer`, `date`,...)
- **VD :** Tạo bảng Persons với 5 cột `PersonID`, `LastName`, `FirstName`, `Address`, `City` :
    ```sql
    CREATE TABLE Persons (
        PersonID int,
        LastName varchar(255),
        FirstName varchar(255),
        Address varchar(255),
        City varchar(255)
    );
    ```
    <img src=https://i.imgur.com/PB66XbH.png>

    Kết quả :

    <img src=https://i.imgur.com/1wHIS7D.png>

### **Tạo bảng dựa trên một bảng khác**
- Có thể sử dụng lệnh `CREATE TABLE` để copy một bảng có sẵn .
- Bảng mới sẽ có các cột và các thuộc tính y hệt bảng ban đầu. Cũng có thể chọn cột được copy sang .
- Nếu tạo một bảng mới dựa trên bảng có sẵn, bảng mới sẽ chứa các giá trị có từ bảng ban đầu .
- Cú pháp :
    ```sql
    CREATE TABLE new_table_name AS SELECT column1, column2,... FROM existing_table_name WHERE ....;
    ```
- **VD :** Copy bảng `Persons` có sẵn, chỉ copy 2 trường `PersonID` và `Lastname` :
    ```sql
    CREATE TABLE Persons_Copy AS SELECT customername, contactname FROM Persons;
    ```
    <img src=https://i.imgur.com/egCy90F.png>

    Kết quả :

    <img src=https://i.imgur.com/ZNPHU6a.png>

    <img src=https://i.imgur.com/7aobKYK.png>
