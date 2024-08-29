# Controller形式のAPIでバージョニングを設定する

Microsoft.AspNetCore.Mvc.Versioning は非推奨。代わりに、Asp.Versioning.Http、Asp.Versioning.Mvc.ApiExplorerパッケージを利用する。

```cs
// APIのバージョニングの設定
builder.Services.AddApiVersioning(options => {
    options.DefaultApiVersion = new ApiVersion(1);
    options.ReportApiVersions = true;
    options.AssumeDefaultVersionWhenUnspecified = true;
    options.ApiVersionReader = ApiVersionReader.Combine(
        new UrlSegmentApiVersionReader(),
        new HeaderApiVersionReader("X-Api-Version"));
}).AddApiExplorer(options => {
    options.GroupNameFormat = "'v'V";
    options.SubstituteApiVersionInUrl = true;
});
```


```cs
[ApiController]
[ApiVersion("1")]
[Route("api/v{v:apiVersion}/[controller]")]
public class ExampleController : ControllerBase {
```
