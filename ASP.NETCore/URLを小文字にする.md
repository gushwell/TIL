# URLを小文字にするには

Startup.csの `ConfigureServices` メソッドで、以下のコードを記述すればよい。

```cs
services.AddRouting(options => options.LowercaseUrls = true);
```

さらに,IdentityHostingStartup,cs の Configure メソッドで以下のように記述する

```cs
  services.ConfigureApplicationCookie(options => {
      options.LoginPath = "/identity/account/login";
      options.ReturnUrlParameter = "returnurl";
  });
```  

なお、このコードは、builder.ConfigureServices` 内のラムダ式の一部。
