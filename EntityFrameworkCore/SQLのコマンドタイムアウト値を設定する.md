## EF Coreで、SQLのコマンドタイムアウト値を設定する

program.csで以下のように記述する.


```cs
var connectionString = builder.Configuration.GetConnectionString("MyDbContext");
builder.Services.AddDbContext<AppDbContext>(options =>
    options.UseSqlServer(connectionString,
                         sqlServerOptions => sqlServerOptions.CommandTimeout(90))
    );

```

CommandTimeoutの引数は、秒を指定する。
