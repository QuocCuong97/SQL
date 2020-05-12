# Lệnh `DROP TABLE`
- Lệnh `DROP TABLE` được sử dụng để xóa một bảng có sẵn trong database .
- Cú pháp :
    ```sql
    DROP TABLE table_name;
    ```
> Cần cẩn thận trước khi xóa Table. Vì việc này đồng nghĩa với xóa tất cả các thông tin lưu trong nó .
- **VD :** Xóa bảng `Persons_Copy` :
    ```sql
    DROP TABLE Persons_Copy;
    ```
    <img src=https://i.imgur.com/yE8AGuH.png>
----------------------
# Lệnh `TRUNCATE TABLE`
- Lệnh `TRUNCATE TABLE` được sử dụng để xóa dữ liệu bên trong bảng , tuy nhiên không xóa bảng .
- Cú pháp :
    ```sql
    TRUNCATE TABLE table_name;
    ```
- **VD :** Xóa dữ liệu bảng `Persons_Copy` :
    ```sql
    TRUNCATE TABLE Persons_Copy;
    ```
    <img src=https://i.imgur.com/zKSVOqY.png>

    Bảng không bị xóa :

    <img src=https://i.imgur.com/fFiE2wB.png>
