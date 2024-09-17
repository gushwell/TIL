# T-SQLでフルバックアップ


```sql
USE SQLTestDB;
GO
BACKUP DATABASE SQLTestDB
TO DISK = 'c:\tmp\SQLTestDB.bak'
   WITH FORMAT,
      MEDIANAME = 'SQLServerBackups',
      NAME = 'Full Backup of SQLTestDB';
GO
```

参考:  
https://docs.microsoft.com/ja-jp/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-ver15
