# Mệnh đề `INSERT INTO`
- Mệnh đề `INSERT INTO` được sử dụng để chèn record mới vào bảng .
- Có thể sử dụng `INSERT INTO` theo 2 cách :
    - Cách 1 : sử dụng cả tên cột và giá trị được chèn vào :
        ```sql
        INSERT INTO table_name (column1, column2, column3, ...) VALUES (value1, value2, value3, ...);
        ```
    - Cách 2 : thêm giá trị mới vào tất cả các cột :
        ```sql
        INSERT INTO table_name VALUES (value1, value2, value3, ...);
        ```