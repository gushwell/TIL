# Azure Functions の Http トリガーのURLにバージョン番号を付加する方法

```cs
[FunctionName(nameof(V1Function))]
public static async Task<HttpResponseMessage> V1Function(
    [HttpTrigger(AuthorizationLevel.Anonymous, "get", "post", Route = "v1/SalesInference")] HttpRequest req,
    ILogger log) {

    ...
    
}

```


HttpTrigger属性の Route パラメータで指定すればよい。
