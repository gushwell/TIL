## ASP.NET Core Web API の Get メソッドで　htmlを返す


以下のようなコードを書く

```cs
  [HttpGet]
  public ContentResult Get()
  {
      var text = "<html><body>Hello World</body></html>");
      return new ContentResult {
          ContentType = "text/html",
          StatusCode = (int)HttpStatusCode.OK,
          Content = text
      };
  }
```

ネットで検索すると`[Produces("text/html")]`のような属性を使うという情報も見つかるがうまくいかない。

この属性を使うならば、StartupのConfigureServicesメソッドでメディアタイプを登録する必要がある。


```cs
services.AddControllers(options => {
    ...
    options.OutputFormatters.OfType<StringOutputFormatter>().Single().SupportedMediaTypes.Add("text/html");
    ...

```
