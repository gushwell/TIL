# program.csでappsettings.jsonの値を取得する

CreateHostBuilderメソッドで以下のような記述をする

```cs
public static IHostBuilder CreateHostBuilder(string[] args) {
    var myValue = false;
    return Host.CreateDefaultBuilder(args)
        .ConfigureAppConfiguration((hostingContext, config) => {
            IConfigurationRoot configuration = config.Build();
            myValue = configuration.GetValue<bool>("myValue");
            if (myValue) {
                ...
            } else {
                ...
            }
        }).ConfigureLogging(logging => {
            ...
            if (myValue) {
                ...
            } else {
               ...
            }
        }).ConfigureWebHostDefaults(webBuilder => {
            webBuilder.UseStartup<Startup>();
        });
}

```

`ConfigureAppConfiguration`内のラムダ式よりも、`ConfigureLogging`, `ConfigureWebHostDefaults` 内のラムダ式のほうが後から呼ばれるはずなので、myValueを参照できる。


`Main`メソッド内でappsettings.jsonの値を参照したければ、以下のようにすれば良い。

```cs
public static void Main(string[] args) {
    var host = CreateHostBuilder(args).Build();
    var config = host.Services.GetRequiredService<IConfiguration>();
    var myValue = config.GetValue<bool>("myValue");
    ...
    host.Run();
}
```
