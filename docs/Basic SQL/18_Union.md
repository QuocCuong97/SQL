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
