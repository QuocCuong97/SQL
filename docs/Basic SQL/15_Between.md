# Toán tử `BETWEEN`
- Toán tử `BETWEEN` lựa chọn giá trị trong 1 khoảng cho trước. Giá trị có thể là number, text hoặc dates .
- Toán tử `BETWEEN` yêu cầu giá trị bắt đầu và giá trị kết thúc của khoảng .
- Cú pháp `BETWEEN` :
    ```sql
    SELECT column_name(s) FROM table_name WHERE column_name BETWEEN value1 AND value2;
    ```
- **VD1 :** Hiển thị các record trên bảng `Persons` với `ID` trong khoảng `2 <= ID <= 4` :
    ```sql
    SELECT * FROM Persons WHERE ID BETWEEN 2 AND 4;
    ```
    <img src=https://i.imgur.com/17Syf18.png>

- **VD2 :** Hiển thị các record trên bảng `Persons` với `ID` KHÔNG trong khoảng `2 <= ID <= 4` :
    ```sql
    SELECT * FROM Persons WHERE ID NOT BETWEEN 2 AND 4;
    ```
    <img src=https://i.imgur.com/7ZHRw0j.png>

- **VD3 :** Hiển thị các record trên bảng `Persons` với `FirstName` trong khoảng `Cuong <= ID <= Tu` :
    ```sql
    SELECT * FROM Persons WHERE FirstName BETWEEN 'Cuong' AND 'Tu';
    ```
