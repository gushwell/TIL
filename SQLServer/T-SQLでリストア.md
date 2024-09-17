# T-SQLでバックアップからデータベースをリストア

LocalDBへリストアする例

```sql
RESTORE DATABASE TestDb
  FROM DISK = 'C:\backup\backup_testdb.bak'
  WITH MOVE 'TestDb' TO 'C:\Users\gushwell\LocalDB\TestDb.mdf',
       MOVE 'TestDb_log' TO 'C:\Users\gushwell\LocalDB\TestDb_log.ldf';
```


AdventureWorksBackups 論理バックアップ デバイスからデータベース バックアップ全体を復元

```sql
RESTORE DATABASE AdventureWorks2022
  FROM AdventureWorks2022Backups;
```


参照URL:  
https://learn.microsoft.com/ja-jp/sql/t-sql/statements/restore-statements-transact-sql?view=sql-server-ver16
