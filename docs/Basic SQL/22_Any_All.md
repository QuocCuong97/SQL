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
    