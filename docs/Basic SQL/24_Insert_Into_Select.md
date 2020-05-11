# Lệnh `INSERT INTO SELECT`
- Lệnh `INSERT INTO SELECT` sẽ copy dữ liệu từ 1 bảng và lồng nó vào trong bảng khác .
    - Lệnh yêu cầu kiểu dữ liệu từ bảng nguồn và bảng đích phải khớp với nhau .
    - Các record đã tồn tại trong bảng đích sẽ không bị ảnh hưởng
- Cú pháp `INSERT INTO SELECT` :
    - Copy toàn bộ các cột từ bảng nọ sang bảng kia :
        ```sql
        INSERT INTO table2 SELECT * FROM table1 WHERE condition;
        ```
    - Copy chỉ một vài cột từ bảng nọ sang bảng kia :
        ```sql
        INSERT INTO table2 (column1, column2, column3, ...) SELECT column1, column2, column3, ... FROM table1 WHERE condition;
        ```
        