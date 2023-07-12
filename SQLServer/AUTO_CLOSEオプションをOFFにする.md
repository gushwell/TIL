# SQL Server の　AUTO_CLOSEオプションをOFFにする。

SQL Server Expressでは、AUTO_CLOSEオプションが規定でONになっている。

これをOFFにすることで、繰り返し並列再実行の started と shutdown が繰り返されるのを回避できる。

以下のコマンドを実行する。

```SQL
ALTER DATABASE <DATABASE_NAME> SET AUTO_CLOSE OFF;
```
