# Giá trị `NULL`
- Một trường với giá trị `NULL` là một trường không có giá trị nào cả .
- Nếu một trường trong bảng là tùy chọn, có thể chèn record mới hoặc update record mà không cần thêm giá trị vào trường đó. Sau đó, trường này sẽ được lưu với giá trị `NULL` .
> Một giá trị `NULL` khác với giá trị `0` hoặc một trường chứa các dấu space . Một trường với giá trị `NULL` là trường bị bỏ trống trong quá trình tạo record .
- Không thể kiểm tra các giá trị `NULL` qua các phép so sánh như `=`, `<`, hoặc `<>` . Thay vì thế ta sẽ sử dụng các toán tử `IS NULL` và `IS NOT NULL` .
- Cú pháp `IS NULL` :
    ```sql
    SELECT column_names FROM table_name WHERE column_name IS NULL;
    ```
- Cú pháp `IS NOT NULL` :
    ```sql
    SELECT column_names FROM table_name WHERE column_name IS NOT NULL;
    ```
- **VD1 :** Kiểm tra xem record nào có giá trị `Address`=`NULL` trong bảng `Persons`:
    ```sql
    SELECT * FROM Persons WHERE Address IS NULL;
    ```
- **VD1 :** Kiểm tra xem record nào có giá trị `Address` KHÔNG `NULL` trong bảng `Persons`:
    ```sql
    SELECT * FROM Persons WHERE Address IS NOT NULL;
    ```