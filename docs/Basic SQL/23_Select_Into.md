# Lệnh `SELECT INTO`
- Lệnh `SELECT INTO` dùng để copy dữ liệu từ 1 bảng vào bảng mới .
- Cú pháp `SELECT INTO` :
    - Copy tất cả các cột của bảng ban đầu vào bảng mới 
        ```sql
        SELECT * INTO newtable [IN externaldb] FROM oldtable WHERE condition;
        ```
    - Copy một số cột vào bảng mới :
        ```sql
        SELECT column1, column2, column3, ... INTO newtable [IN externaldb] FROM oldtable WHERE condition;
        ```
> Bảng mới sẽ được tạo ra với tên cột và kiểu dữ liệu như bảng cũ . Có thể thay để tên cột mới bằng mệnh đề `AS` 