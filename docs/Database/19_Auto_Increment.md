# Trường `AUTO INCREMENT`
- **Auto-increment** cho phép 1 số duy nhất được gen tự động khi mỗi record được chèn vào bảng .
- Thường thì trường có **auto-increment** sẽ là trường **primary key** luôn và có thể tự động được tạo mỗi khi có record mới chèn vào .
- **VD1:** Sử dụng `AUTO INCREMENT` khi tạo bảng :
    ```sql
    CREATE TABLE Persons (
        ID int NOT NULL PRIMARY KEY AUTO_INCREMENT,
        LastName varchar(255),
        FirstName varchar(255),
        Address varchar(255),
        City varchar(255)
    );
    ```
    <img src=https://i.imgur.com/rPPm2Ng.png>
- Mặc định, giá trị bắt đầu của `AUTO_INCREMENT` là `1`, và sẽ tăng lên `1` cho mỗi record mới .
- Để thay đổi giá trị bắt đầu, dùng lệnh sau :
    ```sql
    ALTER TABLE Persons AUTO_INCREMENT=100;
- Khi lưu record, ta sẽ không cần insert giá trị vào cột có thuộc tính `AUTO_INCREMENT` .