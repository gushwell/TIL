# EF CoreのマイグレーションでDB接続先を切り替えたい

## 前提

`appsettings.<Environment>.json`、DBの接続文字列は、それぞれ別のものを設定している。

`<Environment>`には、Development, Staging.json, Production などが入る。


## 方法

以下のようにして切り替える。

Developmentの場合

```
set ASPNETCORE_ENVIRONMENT=Development
dotnet ef database update --context <YourDbContext>
```

これで、`appsettings.Development.json`に書かれたDB接続文字列が利用される。

