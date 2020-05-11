# Lệnh `BACKUP DATABASE`
- Lệnh `BACKUP DATABASE` được sử dụng để tạo bản backup đầy đủ cho một SQL database đã có sẵn .
- Cú pháp :
    ```sql
    BACKUP DATABASE databasename TO DISK = 'filepath';
    ```


--------
# Lệnh `BACKUP WITH DIFFERENTIAL`
- Một **Differential Backup** sẽ chỉ sao lưu phần dữ liệu thay đổi của database kể từ lần sao lưu cuối cùng .
- Cú pháp :
    ```sql
    BACKUP DATABASE databasename TO DISK = 'filepath' WITH DIFFERENTIAL;
    ```
    s