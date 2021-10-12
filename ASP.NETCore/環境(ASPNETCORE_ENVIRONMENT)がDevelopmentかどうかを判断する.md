# 環境(ASPNETCORE_ENVIRONMENT)がDevelopmentかどうかを判断する

PageModel, or Controllerのコンストラクタの引数で、IHostEnvironment を受け取る。

```cs
using Microsoft.Extensions.Hosting;

......
                                    
private IHostEnvironment _env;

public ExampleModel(IHostEnvironment env)
{
  _env = env;
}
```

この_envのIsDevelopmentメソッドを呼び出せば良い。

```cs
if (_env.IsDevelopment())
{
  ....
}
```

