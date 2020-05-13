# Toán tử `EXISTS`
- Toán tử `EXISTS` được sử dụng để kiểm tra sự tồn tại của record trong subquery .
- Toán tử `EXISTS` trả về `true` nếu truy vấn con trả về 1 hoặc nhiều record .
- Cú pháp :
    ```sql
    SELECT column_name(s) FROM table_name WHERE EXISTS (SELECT column_name FROM table_name WHERE condition);
    ```
- **VD :** Có 2 bảng :
    - Bảng `Persons` :

        <img src=https://i.imgur.com/MQ7e8Xx.png>

    - Bảng `Tasks` :

        <img src=https://i.imgur.com/6CX35cu.png>

    - Hiển thị cột `Name` của bảng `Task` với những giá trị có tồn tại cả trong bảng `FirstName` trong bảng `Persons` :S
        ```sql
        SELECT Name FROM Tasks WHERE EXISTS (SELECT FirstName FROM Persons WHERE Tasks.Name=Persons.FirstName);
        ```
        <img src=https://i.imgur.com/HRAhhcn.png>