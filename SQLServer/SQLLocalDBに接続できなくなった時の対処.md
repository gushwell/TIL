SQLLocalDBに接続できなくなった時の対処方法

以下のコマンドを実行

```cmd
sqllocaldb delete MSSQLLocalDB
sqllocaldb create MSSQLLocalDB
```

データベース接続ががすべて消えるが、mdbファイルは消えないので、再度アタッチしてあげれば良い。

