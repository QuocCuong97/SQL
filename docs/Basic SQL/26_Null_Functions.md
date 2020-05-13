# Hàm `IFNULL()`
- Ta có bảng sau :

    <img src=https://i.imgur.com/Of3m9ZL.png>

    - Trong cột `Math` có một giá trị `NULL` .
    - Giả sử ta cần thực hiện truy vấn :
        ```sql
        SELECT FirstName, Math + English AS Total FROM Persons;
        ```
        => Kết quả trả về sẽ là :

        <img src=https://i.imgur.com/Ci1xhvT.png>

> **KẾT LUẬN** : Nếu có bất cứ giá trị nào trong phép tính bị `NULL`, kết quả sẽ trả về `NULL`
- Ta sẽ sử dụng hàm `IFNULL()` để đặt giá trị mặc định thay thế cho các giá trị `NULL` :
    ```sql
    SELECT FirstName, IFNULL(Math, 0) + English AS Total FROM Persons;
    ```
    <img src=https://i.imgur.com/7Vn7cno.png>

    > Giá trị `NULL` trong trường `Math` sẽ được thay thế là `0` .

- Có thể sử dụng hàm `COALESCE()` với cách dùng và kết quả tương tự :
    ```sql
    SELECT FirstName, COALESCE(Math, 0) + English AS Total FROM Persons;
    ```
    <img src=https://i.imgur.com/7XcudSP.png>