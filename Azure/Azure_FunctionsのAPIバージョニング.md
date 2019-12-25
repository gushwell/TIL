# Azure Functions の API バージョニング

HttpTrigger 属性の Route プロパティに、バージョン番号を含んだパスを指定する。
こうすれば、メソッド名、FunctionNameを別の名前にすることができる。

```cs
[FunctionName(nameof(RunV1))]
public static IActionResult RunV1(
    [HttpTrigger(AuthorizationLevel.Function, "get", Route = "v1/hello")] HttpRequest req,
    ILogger log) {
    …
}

[FunctionName(nameof(RunV2))]
public static IActionResult RunV2(
    [HttpTrigger(AuthorizationLevel.Function, "get", Route = "v2/hello")] HttpRequest req,
    ILogger log) {
    …
}

```
