## ASP.NET Core Web API でルート指定

以下のように、Controllerに指定するのが一般的

```cs
    [Route("api/v{version:apiVersion}/[controller]")]
    public class FaceController : ControllerBase
```    

しかし、一部のActionメソッドには、Action名も含めたルートを指定したい場合もある。

そのような場合には、以下のようにActionメソッドにRoute属性を指定すればよい。

```cs
  [Route("[action]")]
  public async Task<ActionResult<Person>> IdentifyAsync(IFormFile postedFile ) {
```

