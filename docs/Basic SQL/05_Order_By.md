# Từ khóa `ORDER BY`
- Từ khóa `ORDER BY` được sử dụng để sắp xếp dữ liệu của ***result-set*** theo thứ tự tăng dần hoặc giảm dần .
- Mặc định từ khóa `ORDER BY` sắp xếp các record theo thứ tự tăng dần . Để sắp xếp các record theo thứ tự giảm dần, sử dụng từ khóa `DESC` .
- Cú pháp `ORDER BY` :
    ```sql
    SELECT column1, column2, ... FROM table_name ORDER BY column1, column2, ... ASC|DESC;
    ```
- **VD1 :** Hiển thị và sắp xếp bảng `Persons` theo cột `FirstName` (thứ tự tăng dần - mặc định):
    ```sql
    SELECT * FROM Persons ORDER BY FirstName;
    ```
    <img src=https://i.imgur.com/eDURUqb.png>

- **VD2 :** Hiển thị và sắp xếp bảng `Persons` theo cột `ID` (thứ tự giảm dần &darr; ):
    ```sql
    SELECT * FROM Persons ORDER BY ID DESC;
    ```
    <img src=https://i.imgur.com/RxuSOvl.png>

- **VD3 :** Hiển thị và sắp xếp bảng `Persons` theo cột `LastName` (thứ tự tăng dần &uarr; ) và `FirstName` (thứ tự tăng dần &uarr; ) :
    ```sql
    SELECT * FROM Persons ORDER BY LastName, FirstName;
    ```
    <img src=https://i.imgur.com/u7Ym170.png>

- **VD4 :** Hiển thị và sắp xếp bảng `Persons` theo cột `LastName` (thứ tự tăng dần &uarr; ) và `FirstName` (thứ tự giảm dần &darr; ) :
    ```sql
    SELECT * FROM Persons ORDER BY LastName ASC, FirstName DESC;
    ```
    <img src=https://i.imgur.com/pmMoBtM.png>