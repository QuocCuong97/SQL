# `AND`, `OR` và `NOT`
- Mệnh đề `WHERE` có thể kết hợp trong đó các toán tử `AND`, `OR` và `NOT` .
- Toán tử `AND` và `OR` được sử dụng để lọc các record dựa trên nhiều hơn 1 điều kiện :
    - Toán tử `AND` hiển thị 1 record nếu tất cả các điều kiện ở các vế của `AND` là True
    - Toán tử `OR` hiển thị 1 record nếu có bất cứ điều kiện nào ở các vế của `OR` là True
- Toán tử `NOT` hiển thị 1 record nếu tất cả các điều kiện đều sai .
- Cú pháp `AND` :
    ```sql
    SELECT column1, column2, ... FROM table_name WHERE condition1 AND condition2 AND condition3 ...;
    ```
- Cú pháp `OR` :
    ```sql
    SELECT column1, column2, ... FROM table_name WHERE condition1 OR condition2 OR condition3 ...;
    ```
- Cú pháp `NOT` :
    ```sql
    SELECT column1, column2, ... FROM table_name WHERE NOT condition;
    ```
- **VD1 :** Tìm kiếm người có `Address` = "`Dong Da`" và `City` = "`Ha Noi`" :
    ```sql
    SELECT * FROM Persons WHERE Address='Dong Da' AND City='Ha Noi';
    ```
    <img src=https://i.imgur.com/UGkPmzF.png>

- **VD2 :** Tìm kiếm người có `Address` = "`Dong Da`" hoặc `LastName` = "`Trang`" :
    ```sql
    SELECT * FROM Persons WHERE Address='Dong Da' OR LastName='Trang';
    ```
    <img src=https://i.imgur.com/Y7974Mn.png>

- **VD3 :** Tìm kiếm người có `Address` KHÔNG PHẢI là "`Dong Da`" :
    ```sql
    SELECT * FROM Persons WHERE NOT Address='Dong Da';
    ```
    <img src=https://i.imgur.com/cZaP4rY.png>

- **VD4 :** Tìm kiếm người có `City` = "`Ha Noi`", `FirstName` = "`Trang`" hoặc "`Tu`" và `Address` KHÔNG PHẢI LÀ "`Hoang Mai`" :
    ```sql
    SELECT * FROM Persons WHERE City='Ha Noi' AND (FirstName='Trang' OR FirstName='Tu') AND (NOT Address='Hoang Mai');
    ```
    <img src=https://i.imgur.com/QRMRrP8.png>