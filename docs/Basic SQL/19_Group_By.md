# Mệnh đề `GROUP BY`
- Mệnh đề `GROUP BY` nhóm các hàng có cùng giá trị vào 1 hàng tổng .
- Mệnh đề `GROUP BY` thường được sử dụng với các hàm tổng hợp (`COUNT`, `MAX`, `MIN`, `SUM`, `AVG`) để nhóm các ***result-set*** được đặt theo một hoặc nhiều cột.
- Cú pháp `GROUP BY` :
    ```sql
    SELECT column_name(s) FROM table_name WHERE condition GROUP BY column_name(s) ORDER BY column_name(s);
    ```