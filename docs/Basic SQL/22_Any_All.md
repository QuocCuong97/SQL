# Toán tử `ANY`, `ALL`
- Toán tử `ANY` và `ALL` được sử dụng trong mệnh đề `WHERE` và `HAVING`
- Toán từ `ANY` trả về `true` nếu có bất cứ giá trị subquery nào match với điều kiện .
- Toán từ `ALL` trả về `true` nếu tất cả các giá trị subquery match với điều kiện .
- Cú pháp `ANY` :
    ```sql
    SELECT column_name(s) FROM table_name WHERE column_name operator ANY (SELECT column_name FROM table_name WHERE condition);
    ```
- Cú pháp `ALL` :
    ```sql
    SELECT column_name(s) FROM table_name WHERE column_name operator ALL (SELECT column_name FROM table_name WHERE condition);
    ```
- **VD :** Có 2 bảng :
    - Bảng `Persons` :

        <img src=https://i.imgur.com/MQ7e8Xx.png>

    - Bảng `Tasks` :

        <img src=https://i.imgur.com/6CX35cu.png>

- **VD1 :** Hiển thị cột `Name` và `Task` của bảng `Task` nếu cột `Name` có bất cứ giá trị nào nằm trong kết quả truy vấn trả về của cột `FirstName` trong bảng `Persons` với `ID >= 2`
    ```sql
    SELECT Name, Task FROM Tasks WHERE Name = ANY (SELECT FirstName FROM Persons WHERE ID >= 2);
    ```
    <img src=https://i.imgur.com/gHyH58d.png>

- **VD2 :** Hiển thị cột `Name` và `Task` của bảng `Task` nếu cột `Name` có tất cả giá trị nào nằm trong kết quả truy vấn trả về của cột `FirstName` trong bảng `Persons` với `ID >= 2` . Nếu cột có `ID < 2` thì không có kết quả trả về :
    ```sql
    SELECT Name, Task FROM Tasks WHERE Name = ALL (SELECT FirstName FROM Persons WHERE ID >= 2);
    ```
    <img src=https://i.imgur.com/x5QC7BW.png>
