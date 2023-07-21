# プログラム実行時に、EF CoreのDBマイグレーションを行いたい

開発時は、`dotnet ef database update` でDBのマイグレーションを行うことが多いが、C#のプロジェクトファイルがない環境でプログラム実行時に同様のことを行いたい場合がある。

このような時には、C# の Program.cs　で以下のようなコードを書けば良い。

```cs
using (var scope = app.Services.CreateScope())
{
    var services = scope.ServiceProvider;
    var dbContext = services.GetService<AppDbContext>();
    if (dbContext != null)
    {
        if (dbContext.Database.GetPendingMigrations().Any())
            dbContext.Database.Migrate();
    }
}
```
