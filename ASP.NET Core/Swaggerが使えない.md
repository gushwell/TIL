# ASP.NET Core 3.0 で Swagger が使えない

ASP.NET Core 3.0 で Swagger 使おうと思ったら、なんかわけのわからないエラーが出てしまう。

```
TypeLoadException: Could not load type 'Microsoft.AspNetCore.Mvc.MvcJsonOptions' from assembly 'Microsoft.AspNetCore.Mvc.Formatters.Json, Version=3.0.0.0, Culture=neutral, PublicKeyToken=adb9793829ddae60'.
```

とか

```
  Message=Method not found: 'Void Microsoft.AspNetCore.StaticFiles.StaticFileMiddleware..ctor(Microsoft.AspNetCore.Http.RequestDelegate, Microsoft.AspNetCore.Hosting.IHostingEnvironment, Microsoft.Extensions.Options.IOptions`1<Microsoft.AspNetCore.Builder.StaticFileOptions>, Microsoft.Extensions.Logging.ILoggerFactory)'.
  Source=Swashbuckle.AspNetCore.SwaggerUI
```

とか。

調べたら、

パッケージが rc4 のやつを入れないとダメだった。

```
Install-Package Swashbuckle.AspNetCore -Version 5.0.0-rc4
```

これで、うまく動作するようになった。

