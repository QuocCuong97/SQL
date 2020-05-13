# Lệnh `DELETE`
- Mệnh đề `DELETE` được sử dụng để xóa record có sẵn trong bảng .
- Cú pháp `DELETE` :
    ```sql
    DELETE FROM table_name WHERE condition;
    ```
- **VD1 :** Xóa record trong bảng `Persons` ở dòng có `ID` = `1` :
    ```sql
    DELETE FROM Persons WHERE ID=1;
    ```
- **VD2 :** Xóa tất cả các record trong bảng `Persons` :
    ```sql
    DELETE FROM Persons;
    ```
