# Toán tử `LIKE`
- Toán tử `LIKE` được sử dụng trong mệnh đề `WHERE` để tìm kiếm một mẫu chỉ định trước trong cột .
- Có 2 ký tự đại diện được sử dụng với toán tử `LIKE` :
    - `%` : Đại diện cho `0`, `1` hoặc nhiều ký tự .
    - `_` : Đại diện cho 1 ký tự .
    > Cả 2 kí tự cũng có thể được sử dụng kết hợp .
- Cú pháp `LIKE` :
    ```sql
    SELECT column1, column2, ... FROM table_name WHERE columnN LIKE pattern;
    ```
- Các mẫu sử dụng toán tử `LIKE` :

    | Mệnh đề chứa `LIKE` | Mô tả |
    |---------------------|-------|
    | `WHERE Name LIKE 'a%'` | Tìm bất cứ giá trị nào bắt đầu bằng `a` |
    | `WHERE Name LIKE '%a'` | Tìm bất cứ giá trị nào kết thúc bằng `a` |
    | `WHERE Name LIKE '%or%'` | Tìm bất cứ giá trị nào chứa `or` |
    | `WHERE Name LIKE '_r%'` | Tìm bất cứ giá trị nào có `r` là kí tự ở vị trí thứ 2 | 
    | `WHERE Name LIKE 'a_%'` | Tìm bất cứ giá trị nào bắt đầu bằng `a` và có tối thiểu 2 kí tự |
    | `WHERE Name LIKE 'a__%'` | Tìm bất cứ giá trị nào bắt đầu bằng `a` và có tối thiểu 3 kí tự |
    | `WHERE Name LIKE 'a%o'` | Tìm bất cứ giá trị nào bắt đầu bằng `a` và kết thúc bằng `o` |