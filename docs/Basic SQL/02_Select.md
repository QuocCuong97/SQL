# `SELECT`
- Cú pháp `SELECT` được sử dụng để lấy dữ liệu từ database .
- Dữ liệu trả về được lưu dưới dạng bảng kết quả, gọi là ***result-set*** .
- Cú pháp : 
    ```sql
    SELECT column1, column2, ... FROM table_name;
    ```
    - Trong đó : `column1`, `column2`,... là tên các trường (field) trong bảng mà muốn lấy dữ liệu. 
    - Có thể lấy tất các các trường của bảng bằng cú pháp :
        ```sql
        SELECT * FROM table_name;
        ```
# `SELECT DISTINCT`
- Cú pháp `SELECT DISTINCT` được sử dụng để trả về các giá trị riêng biệt trong cột .
- Trong 1 bảng, một cột thường bao gồm nhiều trường giá trị trùng lặp; thi thoảng người dùng chỉ muốn liệt kê ra các giá trị khác nhau .
- Cú pháp :
    ```sql
    SELECT DISTINCT column1, column2, ... FROM table_name;
    ```
