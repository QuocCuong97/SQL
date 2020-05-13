# Lệnh `UPDATE`
- Cú pháp `UPDATE` được dùng để sửa các record có sẵn trong bảng .
- Cú pháp `UPDATE` :
    ```sql
    UPDATE table_name SET column1 = value1, column2 = value2, ... WHERE condition;
    ```
- **VD1 :** Update dữ liệu cho bảng `Persons` ở dòng có `ID` = `1`, sửa `FirstName` thành "`Tuan`" :
    ```sql
    UPDATE Persons SET FirstName='Tuan' WHERE ID = 1;
    ```
    <img src=https://i.imgur.com/kG3B6QQ.png>

> **CHÚ Ý :** Nếu bỏ qua mệnh đề `WHERE`, tất cả các record sẽ được update .
