# Toán tử `UNION`
- Toán tử `UNION` được sử dụng để kết hợp các ***result-set*** của 2 hoặc nhiều mệnh đề `SELECT` .
    - Mỗi mệnh đề `SELECT` không có `UNION` phải giống nhau về số cột .
    - Các cột phải có cùng kiểu dữ liệu .
    - Các cột trong mỗi mệnh đề `SELECT` phải cùng thứ tự
- Cú pháp `UNION` :
    ```sql
    SELECT column_name(s) FROM table1 UNION SELECT column_name(s) FROM table2;
    ```
- Cú pháp `UNION ALL` :
    ```sql
    SELECT column_name(s) FROM table1 UNION ALL SELECT column_name(s) FROM table2;
    ```
> Tên cột trả về trong ***result-set*** thường là tên cột của mệnh đề `SELECT` thứ nhất trong cú pháp `UNION` .
- **VD :** Có 2 bảng :
    - Bảng `Persons` :

        <img src=https://i.imgur.com/MQ7e8Xx.png>

    - Bảng `Tasks` :

        <img src=https://i.imgur.com/6CX35cu.png>

    - Kết hợp cột `FirstName` của bảng `Persons` và cột `Name` của bảng `Tasks` khi hiển thị (đã bỏ qua các giá trị trùng nhau):
        ```sql
        SELECT FirstName FROM Persons UNION SELECT Name FROM Tasks;
        ```
        <img src=https://i.imgur.com/oM1pixu.png>

    - Kết hợp cột `City` của bảng `Persons` và cột `Task` của bảng `Tasks` khi hiển thị (đã bỏ qua các giá trị trùng nhau):
        ```sql
        SELECT City FROM Persons UNION SELECT Task FROM Tasks;
        ```
        <img src=https://i.imgur.com/xMuwMsd.png>