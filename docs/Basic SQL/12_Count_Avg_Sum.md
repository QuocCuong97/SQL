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