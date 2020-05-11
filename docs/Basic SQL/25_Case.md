# Lệnh `CASE`
- Lệnh `CASE` đi qua các điều kiện và trả về giá trị khi điều kiện đầu tiên được đáp ứng ( như `IF-THEN-ELSE` ) . Vì vậy, khi một điều kiện là đúng, nó sẽ dừng đọc điều kiện và trả về kết quả luôn. Nếu không có điều kiện nào đúng, nó sẽ trả về kết quả của mệnh đề `ELSE` .
- Nếu không có phần `ELSE` trong lệnh và không có điều kiện nào đúng, nó sẽ trả về `NULL` .
- Cú pháp :
    ```sql
    CASE WHEN condition1 THEN result1 WHEN condition2 THEN result2 WHEN conditionN THEN resultN ELSE result END;
    ```
