# 複数のDBがある場合のMigration方法

--context オプションを使う。

```
dotnet ef migrations add initialCreate --context myDbContext

dotnet ef database update --context myDbContext
```

DBの削除は、

``` 
dotnet ef database drop --context myDbContext
```

マイグレーションをやり直すには、(DB削除後に実行)

``` 
dotnet ef migrations remove --context myDbContext
```
