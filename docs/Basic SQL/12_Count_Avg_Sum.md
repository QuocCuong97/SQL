# Hàm `COUNT()`, `AVG()` và `SUM()`
- Hàm `COUNT()` trả về số lượng hàng (row) khớp với tiêu chí đã chỉ định .
- Hàm `AVG()` trả về giá trị trung bình của một cột gồm các giá trị số .
- Hàm `SUM()` trả về giá trị tổng cộng của một cột gồm các giá trị số .
- Cú pháp hàm `COUNT()` :
    ```sql
    SELECT COUNT(column_name) FROM table_name WHERE condition;
    ```
- Cú pháp hàm `AVG()` :
    ```sql
    SELECT AVG(column_name) FROM table_name WHERE condition;
    ```
- Cú pháp hàm `SUM()` :
    ```sql
    SELECT SUM(column_name) FROM table_name WHERE condition;
    ```
- Ta có bảng `Persons` :

    <img src=https://i.imgur.com/pyyxzqi.png>

- **VD1 :** Đếm số record trong bảng dựa trên cột `Address` :
    ```sql
    SELECT COUNT(Address) FROM Persons;
    ```
    <img src=https://i.imgur.com/hXDY3On.png>

- **VD2 :** Đếm số record có `LastName`="`Ngo Quoc`" trong bảng dựa trên cột `ID` :
    ```sql
    SELECT COUNT(ID) FROM Persons WHERE LastName='Ngo Quoc';
    ```
    <img src=https://i.imgur.com/h0xPykt.png>

- **VD3 :** Tính trung bình cộng cột `Math` :
    ```sql
    SELECT AVG(Math) FROM Persons;
    ```
    <img src=https://i.imgur.com/8DC6rSE.png>

- **VD4 :** Tính trung bình cộng cột `Math` những record có `FirstName` bắt đầu bằng `T` :
    ```sql
    SELECT AVG(Math) FROM Persons WHERE FirstName LIKE 'T%';
    ```
    <img src=https://i.imgur.com/rXfogWi.png>

- **VD5 :** Cộng tổng cột `English` :
    ```sql
    SELECT SUM(English) FROM Persons;
    ```
    <img src=https://i.imgur.com/Zdm5q2K.png>

- **VD6 :** Cộng tổng cột `English` những record có `LastName` là `Ngo Quoc` :
    ```sql
    SELECT SUM(English) FROM Persons WHERE LastName='Ngo Quoc';
    ```
    <img src=https://i.imgur.com/SHoqMEd.png>