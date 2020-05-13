# Hàm `MIN()` và `MAX()`
- Hàm `MIN()` trả về giá trị nhỏ nhất của cột được chọn
- Hàm `MAX()` trả về giá trị lớn nhất của cột được chọn
- Cú pháp `MIN()` :
    ```sql
    SELECT MIN(column_name) FROM table_name WHERE condition;
    ```
- Cú pháp `MAX()` :
    ```sql
    SELECT MAX(column_name) FROM table_name WHERE condition;
    ```
- Ta có bảng `Persons` :

    <img src=https://i.imgur.com/pyyxzqi.png>

- **VD1 :** Tìm số nhỏ nhất trong cột `Math` và thay tên tột thành `Lowest Math` :
    ```sql
    SELECT MIN(Math) AS 'Lowest Math' FROM Persons;
    ```
    <img src=https://i.imgur.com/sP9jPYy.png>
    
- **VD2 :** Tìm số lớn nhất trong cột `Math` và thay tên tột thành `Highest Math` :
    ```sql
    SELECT MAX(Math) AS 'Highest Math' FROM Persons;
    ```
    <img src=https://i.imgur.com/KpCYZWM.png>
