# Lệnh `BACKUP DATABASE`
- Lệnh `BACKUP DATABASE` được sử dụng để tạo bản backup đầy đủ cho một SQL database đã có sẵn .
- Cú pháp :
    ```sql
    BACKUP DATABASE databasename TO DISK = 'filepath';
    ```
- **VD :** Backup database "`testDB`" :
    ```
    BACKUP DATABASE testDB TO DISK = '\home\cuongnq\testDB.bak';
    ```
> Chú ý : Nên backup file database sang ổ đĩa khác với ổ đĩa chạy MySQL. Phòng trường hợp dữ liệu trên ổ đĩa chính bị crash, 
--------
# Lệnh `BACKUP WITH DIFFERENTIAL`
- Một **Differential Backup** sẽ chỉ sao lưu phần dữ liệu thay đổi của database kể từ lần sao lưu cuối cùng .
- Cú pháp :
    ```sql
    BACKUP DATABASE databasename TO DISK = 'filepath' WITH DIFFERENTIAL;
    ```
- **VD :** Backup database "`testDB`" :
    ```
    BACKUP DATABASE testDB TO DISK = '\home\cuongnq\testDB.bak' WITH DIFFERENTIAL;
    ```