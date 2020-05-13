# SQL Comments
- Comment được sử dụng để giải thích các phần trong lệnh SQL, hoặc để chặn việc thực thi lệnh SQL .
- Comment thường được sử dụng trong file thực thi `.sql`
- **VD1 :** Comment 1 dòng :
    ```sql
    --Select all:
    SELECT * FROM Persons;
    ```
    hoặc
    ```sql
    SELECT * FROM Persons -- WHERE City='Ha Noi';
    ```
- **VD2 :** Comment nhiều dòng :
    ```sql
    /*Select all the columns
    of all the records
    in the Customers table:*/
    SELECT * FROM Persons;
    ```