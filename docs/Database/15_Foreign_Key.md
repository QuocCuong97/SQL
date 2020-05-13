# Constraint `FOREIGN KEY`
- `FOREIGN KEY` là key để kết nối 2 bảng lại với nhau .
- Một `FOREIGN KEY` là một cột (hoặc tập hợp nhiều cột) trong một bảng và chính là `PRIMARY KEY` của bảng khác .
- Bảng chứa **foreign key** được gọi là **child table**, và bảng chứa **primary key** liên kết bới nó được gọi là **referenced table** (bảng tham chiếu) hoặc **parent table** (bảng cha) .
- **VD :** Bảng `Person` - bảng tham chiếu :

    <img src=https://i.imgur.com/1D4nc5h.png>

- **VD1 :** Tạo bảng `Marks` sử dụng `FOREIGN KEY` tham chiếu đến bảng `Persons` :
    ```sql
    CREATE TABLE Marks (
        MarkID int NOT NULL PRIMARY KEY,
        Math int NOT NULL,
        English int NOT NULL,
        PersonID int,
        FOREIGN KEY (PersonID) REFERENCES Persons(ID)
    );
    ```
    <img src=https://i.imgur.com/QpAfSEn.png>

- **VD2 :** Đặt tên cho `FOREIGN KEY` ( trường hợp có thể sử dụng cho việc dùng nhiều cột làm `FOREIGN KEY` ) :
    ```sql
    CREATE TABLE Marks (
        MarkID int NOT NULL PRIMARY KEY,
        Math int NOT NULL,
        English int NOT NULL,
        PersonID int,
        CONSTRAINT FK_Persons FOREIGN KEY (PersonID) REFERENCES Persons(ID)
    );
    ```
- **VD3 :** Thêm `FOREIGN_KEY` khi bảng `Marks` đã có sẵn :
    ```sql
    ALTER TABLE Marks ADD FOREIGN KEY (PersonID) REFERENCES Persons(ID);
    ```
- **VD4 :** Xóa `FOREIGN_KEY` đã được gán sẵn :
    ```sql
    ALTER TABLE Marks DROP FOREIGN KEY FK_Persons;
    ```
    