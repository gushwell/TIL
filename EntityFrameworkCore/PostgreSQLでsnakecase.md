## テーブル名、カラム名をsnake case に変更する

以下のパッケージをNugetでインストール

```
EFCore.NamingConventions
```

DbContextクラスで、OnConfiguring を以下のように書く。

```c#
   protected override void OnConfiguring(DbContextOptionsBuilder optionsBuilder) {
        var conn = _config.GetConnectionString(nameof(AppDbContext));
        optionsBuilder.UseNpgsql(conn)
                      .UseSnakeCaseNamingConvention();
    }
```        
        
UseSnakeCaseNamingConvention() 拡張メソッドを呼ぶことで、snake case にすることができる。

----
GitHUb にドキュメントがある

https://github.com/efcore/EFCore.NamingConventions


