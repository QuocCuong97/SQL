# Mệnh đề `WHERE`
- Mệnh đề `WHERE` được sử dụng để lọc record .
- Mệnh đề `WHERE` được sử dụng để trích xuất các record đáp ứng những điều kiện cụ thể .
- Cú pháp :
    ```sql
    SELECT column1, column2, ... FROM table_name WHERE condition;
    ```
    > Mệnh đề `WHERE` không chỉ được sử dụng cùng với `SELECT` mà còn đi cùng `UPDATE`, `DELETE`,...

- **VD1 :** Tìm kiếm người có `Address` = "`Dong Da`" trong bảng `Persons` :
    ```sql
    SELECT * from Persons WHERE Address='Dong Da';
    ```
    <img src=https://i.imgur.com/udzNlcc.png>

- **SQL** yêu cầu dấu nháy đơn (`''`) quanh trường text, tuy nhiên nếu là số thì không cần .
- **VD2 :** Tìm kiếm người có `ID` = `2` trong bảng `Persons` :
    ```sql
    SELECT * from Persons WHERE ID=2;
    ```
    <img src=https://i.imgur.com/GNtPUVA.png>