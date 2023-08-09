## builder.Build() する前

```cs
var sp = builder.services.BuildServiceProvider();
var value = sp.GetService<IOptions<AppConfig>>()?.Value;
```

これで、AppConfigクラスの各プロパティにappsettings.jsonの値が設定される。



## builder.Build() した後

```cs
var value = app.Configuration.GetSection("AppConfig").Get<AppConfig>();
```

これで、AppConfigクラスの各プロパティにappsettings.jsonの値が設定される。
