# Alias
- SQL Alias được sử dụng để cho 1 bảng, 1 cột trong bảng 1 cái tên tạm thời .
- Alias thường được sử dụng để giúp cho tên cột dễ đọc hơn .
- Một alias chỉ tồn tại trong thời hạn của query .
- Cú pháp alias cho cột :
    ```sql
    SELECT column_name AS alias_name FROM table_name;
    ```
- Cú pháp alias cho bảng :
    ```sql
    SELECT column_name(s) FROM table_name AS alias_name;
    ```