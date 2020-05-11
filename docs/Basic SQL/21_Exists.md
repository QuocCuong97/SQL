# Toán tử `EXISTS`
- Toán tử `EXISTS` được sử dụng để kiểm tra sự tồn tại của record trong subquery .
- Toán tử `EXISTS` trả về `true` nếu truy vấn con trả về 1 hoặc nhiều record .
- Cú pháp :
    ```sql
    SELECT column_name(s) FROM table_name WHERE EXISTS (SELECT column_name FROM table_name WHERE condition);
    ```