# WebAPIでグローバルフィルターを設定する

## Filterクラスを定義する

例えば、`IExceptionFilter`を実装したクラス。

```cs
    public class MyExceptionFilter : IExceptionFilter {

        public MyExceptionFilter() {
            
        }

        public void OnException(ExceptionContext context) {
            ...
        }
    }

```

## Startup.cs で組み込む

```cs
      services.AddControllers(options => {
          options.Filters.Add<MyExceptionFilter>();
      });
```            
