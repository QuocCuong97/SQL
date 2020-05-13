# Mệnh đề `LIMIT`
- Mệnh đề `LIMIT` được sử dụng để chỉ định số record trả về sau câu truy vấn .
- Mệnh đề `LIMIT` rất hữu dụng trên các bảng lớn với hàng nghìn record. Nếu truy vấn một số lượng lớn record sẽ ảnh hưởng đến hiệu năng server .
- Cú pháp :
    ```sql
    SELECT column_name(s) FROM table_name WHERE condition LIMIT number;
    ```
- **VD1 :** Hiển thị 3 dòng đầu của bảng `Persons` :
    ```sql
    SELECT * FROM Persons LIMIT 3;
    ```
    <img src=https://i.imgur.com/isGq4fk.png>

- **VD2 :** Hiển thị 1 record đầu tiên có `LastName` = "`Ngo Quoc`" của bảng `Persons` :
    ```sql
    SELECT * FROM Persons WHERE LastName='Ngo Quoc' LIMIT 1;
    ```
    <img src=https://i.imgur.com/s6VGAxx.png>