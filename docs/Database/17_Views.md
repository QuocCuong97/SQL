# Lệnh `VIEWS`
- Trong **SQL**, một **view** là một bảng ảo (virtual table) dựa trên ***result-set*** trả về từ một truy vấn **SQL** .
- Một **view** chứa cột, hàng, giống như một bảng thật. Các trường trong **view** là các trường từ một hoặc nhiều bảng thật trong database .
- Có thể thêm các SQL function, `WHERE`, `JOIN` vào **view** để hiển thị **view**
- Cú pháp :
    ```sql
    CREATE VIEW view_name AS SELECT column1, column2, ... FROM table_name WHERE condition;
    ```