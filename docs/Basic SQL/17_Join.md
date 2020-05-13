# SQL Join
- Mệnh đề `JOIN` được sử dụng để gộp các hàng từ 2 hay nhiều bảng, dựa trên 1 cột chung giữa chúng .
- Có nhiều loại `JOIN` trong SQL :
    - `(INNER) JOIN` : Trả về các record có giá trị khớp trong cả 2 bảng
    - `LEFT (OUTER) JOIN` : Trả về tất cả các record từ bảng bên trái và các record khớp từ bảng bên phải
    - `RIGHT (OUTER) JOIN` : Trả về tất cả các record từ bảng bên phải và các record khớp từ bảng bên trái
    - `FULL (OUTER) JOIN` : Trả về tất cả các record khớp với nhau trên cả 2 bảng
    - `(SELF) JOIN` : 



<img src=https://i.imgur.com/rPTuE4G.gif>

<img src=https://i.imgur.com/F0FPFDC.gif>

<img src=https://i.imgur.com/iIQett6.gif>

<img src=https://i.imgur.com/bQROg2r.gif>

### **INNER JOIN**
- Cú pháp :
    ```sql
    SELECT column_name(s) FROM table1 INNER JOIN table2 ON table1.column_name = table2.column_name;
    ```
- **VD :** Có 2 bảng :
    - Bảng `Persons` :

        <img src=https://i.imgur.com/MQ7e8Xx.png>

    - Bảng `Tasks` :

        <img src=https://i.imgur.com/6CX35cu.png>

- JOIN bảng `Persons` và bảng `Tasks` dựa vào cột `FirstName` trong bảng `Persons` :
    ```sql
    SELECT Persons.*, Tasks.Task FROM Persons INNER JOIN Tasks ON Persons.FirstName=Tasks.Name;
    ```
    <img src=https://i.imgur.com/rAQMx29.png>
- [INNER JOIN 3 Bảng](https://www.w3schools.com/sql/sql_join_inner.asp)
### **LEFT (OUTER) JOIN**
- Cú pháp :
    ```sql
    SELECT column_name(s) FROM table1 LEFT JOIN table2 ON table1.column_name = table2.column_name;
    ```
- **VD :** Có 2 bảng :
    - Bảng `Persons` :

        <img src=https://i.imgur.com/MQ7e8Xx.png>

    - Bảng `Tasks` :

        <img src=https://i.imgur.com/6CX35cu.png>

- JOIN bảng `Persons` và bảng `Tasks` dựa vào cột `FirstName` trong bảng `Persons` :
    ```sql
    SELECT Persons.LastName, Persons.FirstName, Tasks.Task FROM Persons LEFT JOIN Tasks ON Persons.FirstName=Tasks.Name;
    ```
    <img src=https://i.imgur.com/pVwQVFq.png>

### **RIGHT (OUTER) JOIN**
- Cú pháp :
    ```sql
    SELECT column_name(s) FROM table1 RIGHT JOIN table2 ON table1.column_name = table2.column_name;
    ```
- **VD :** Có 2 bảng :
    - Bảng `Persons` :

        <img src=https://i.imgur.com/MQ7e8Xx.png>

    - Bảng `Tasks` :

        <img src=https://i.imgur.com/6CX35cu.png>

- JOIN bảng `Persons` và bảng `Tasks` dựa vào cột `FirstName` trong bảng `Persons` :
    ```sql
    SELECT Persons.LastName, Persons.FirstName, Task.Name, Tasks.Task FROM Persons RIGHT JOIN Tasks ON Persons.FirstName=Tasks.Name;
    ```
    <img src=https://i.imgur.com/6hfEzbD.png>

### **FULL (OUTER) JOIN**
- Cú pháp :
    ```sql
    SELECT column_name(s) FROM table1 FULL OUTER JOIN table2 ON table1.column_name = table2.column_name WHERE condition;
    ```
- **VD :** Có 2 bảng :
    - Bảng `Persons` :

        <img src=https://i.imgur.com/MQ7e8Xx.png>

    - Bảng `Tasks` :

        <img src=https://i.imgur.com/6CX35cu.png>

- JOIN bảng `Persons` và bảng `Tasks` dựa vào cột `FirstName` trong bảng `Persons` :
    ```sql
    SELECT Persons.LastName, Persons.FirstName, Task.Name, Tasks.Task FROM Persons FULL OUTER JOIN Tasks ON Persons.FirstName=Tasks.Name;
    ```
    ```
    ???
    ```
### **SELF JOIN**
- Cú pháp :
    ```sql
    SELECT column_name(s) FROM table1 T1, table1 T2 WHERE condition;
    ```
- **VD :**
    ```
    ???
    ```
    