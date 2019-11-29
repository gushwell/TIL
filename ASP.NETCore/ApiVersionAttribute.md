# ApiVersionAttribute

 Nugetから Microsoft.AspNetCore.Mvc.Versioning をインストールすることで、利用可能になる。
 
 
 ```c#
         public void ConfigureServices(IServiceCollection services) {
            ...
            services.AddApiVersioning(
                 options => {
                    options.ReportApiVersions = true;
                 });
        }
 ```
 
 ```c#
    [ApiController]
    [ApiVersion("1.0")]
    [Route("api/v{version:apiVersion}/[controller]")]
    public class HomeController : ControllerBase
```    

これで、以下のURLで Web API を呼び出せるようになる。

```
https://example.com/api/v1/home/
```

2つのバージョンをサポートする場合は、以下のようにすると良い。

 ```c#
    [ApiController]
    [ApiVersion("1.0")]
    [ApiVersion("2.0")]
    [Route("api/v{version:apiVersion}/[controller]")]
    public class HomeController : ControllerBase
```    

サポート外のバージョンを指定すると http status 400 が返る。以下、応答本文の例

```
{"error":{"code":"UnsupportedApiVersion","message":"The HTTP resource that matches the request URI 'https://localhost:44333/api/v2/novel' does not support the API version '2'.","innerError":null}}
```

コントローラー名にバージョンを入れたいこともある。以下のように書く。

```c#
services.AddApiVersioning(o => {
 o.ReportApiVersions = true;
 o.AssumeDefaultVersionWhenUnspecified = true;
 o.DefaultApiVersion = new ApiVersion(1, 0);
 
 o.Conventions.Controller<HomeV1Controller>().HasApiVersion(new ApiVersion(1, 0));
 o.Conventions.Controller<HomeV2Controller>().HasApiVersion(new ApiVersion(2, 0));
});
```

コントローラが多いと面倒だが、現実問題、コントローラー数が多くなることはまれだと思われる。
