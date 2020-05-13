# Mệnh đề `GROUP BY`
- Mệnh đề `GROUP BY` nhóm các hàng có cùng giá trị vào 1 hàng tổng .
- Mệnh đề `GROUP BY` thường được sử dụng với các hàm tổng hợp (`COUNT`, `MAX`, `MIN`, `SUM`, `AVG`) để nhóm các ***result-set*** được đặt theo một hoặc nhiều cột.
- Cú pháp `GROUP BY` :
    ```sql
    SELECT column_name(s) FROM table_name WHERE condition GROUP BY column_name(s) ORDER BY column_name(s);
    ```
- **VD1 :** Trong bảng `Persons`, nhóm các giá trị giống nhau trong cột `LastName` và đếm theo cột `ID` :
    ```sql
    SELECT COUNT(ID), LastName FROM Persons GROUP BY LastName;
    ```
    <img src=https://i.imgur.com/8KPEevf.png>