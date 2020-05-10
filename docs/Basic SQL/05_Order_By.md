# Từ khóa `ORDER BY`
- Từ khóa `ORDER BY` được sử dụng để sắp xếp dữ liệu của ***result-set*** theo thứ tự tăng dần hoặc giảm dần .
- Mặc định từ khóa `ORDER BY` sắp xếp các record theo thứ tự tăng dần . Để sắp xếp các record theo thứ tự giảm dần, sử dụng từ khóa `DESC` .
- Cú pháp `ORDER BY` :
    ```sql
    SELECT column1, column2, ... FROM table_name ORDER BY column1, column2, ... ASC|DESC;
    ```