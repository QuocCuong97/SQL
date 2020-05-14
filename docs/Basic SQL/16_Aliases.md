# Alias
- SQL Alias được sử dụng để cho 1 bảng, 1 cột trong bảng 1 cái tên tạm thời .
- Alias thường được sử dụng để giúp cho tên cột dễ đọc hơn .
- Một alias chỉ tồn tại trong thời hạn của query .
- Cú pháp alias cho cột :
    ```sql
    SELECT column_name AS alias_name FROM table_name;
    ```
- Cú pháp alias cho bảng :
    ```sql
    SELECT column_name(s) FROM table_name AS alias_name;
    ```
- **VD1 :** Hiển thị cột `ID` với tên thay thế là "`STT`", cột `LastName` -> "`Ho`", cột `FirstName` -> "`Ten`", `Address` -> "`Dia Chi`", `City` -> "`Thanh Pho`" :
    ```sql
    SELECT ID AS STT, LastName AS Ho, FirstName AS Ten, Address AS 'Dia Chi', City AS 'Thanh Pho' FROM Persons;
    ```
    <img src=https://i.imgur.com/OmxvFCN.png>

> Đặt tên cột mới trong dấu `''` hoặc `[]` nếu trong tên cột mới có chứa dấu cách .
### Sử dụng hàm `CONCAT()`
- **VD2 :** Gộp 2 cột `LastName` và `FirstName` thành 1 cột `Full Name` , 2 cột `Address` và `City` lại thành 1 cột `Full Address` :
    ```sql
    SELECT ID, CONCAT(LastName, ' ', FirstName) AS 'Full Name', CONCAT(Address, ', ', City) AS 'Full Address' FROM Persons;
    ```
    ```
    Đoạn này đang lỗi. Cần kiểm chứng lại
    ```
