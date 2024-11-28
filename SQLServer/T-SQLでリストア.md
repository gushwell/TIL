# T-SQLでバックアップからデータベースをリストア

### LocalDBへリストアする例

```sql
RESTORE DATABASE TestDb
  FROM DISK = 'C:\backup\backup_testdb.bak'
  WITH MOVE '論理ファイル名_Data' TO 'C:\Users\gushwell\LocalDB\TestDb.mdf',
       MOVE '論理ファイル名_Log' TO 'C:\Users\gushwell\LocalDB\TestDb_log.ldf';
```

'論理ファイル名_Data','論理ファイル名_Log'は、以下のクエリを実行すると取得できる。


```sql
RESTORE FILELISTONLY
FROM DISK = 'C:\backup\backup_testdb.bak';
```

### 論理バックアップ デバイスからデータベース バックアップ全体を復元する例

```sql
RESTORE DATABASE AdventureWorks2022
  FROM AdventureWorks2022Backups;
```


参照URL:  
https://learn.microsoft.com/ja-jp/sql/t-sql/statements/restore-statements-transact-sql?view=sql-server-ver16
