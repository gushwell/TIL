# 複数のDBがある場合のMigration方法

--context オプションを使う。

```
dotnet ef migrations add initialCreate --context myDbContext

dotnet ef database update --context myDbContext
```

削除は、

``` 
dotnet ef database drop --context myDbContext
```
