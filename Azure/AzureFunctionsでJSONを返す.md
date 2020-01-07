# Azure Functions で JSONを返す

```cs
    [FunctionName(nameof(V1Function))]
    public static async Task<HttpResponseMessage> V1Function(
        [HttpTrigger(AuthorizationLevel.Anonymous, "get", "post", Route = "v1/SalesInference")] HttpRequest req,
        ILogger log) {
        ...
            
        var jsonToReturn = JsonConvert.SerializeObject(results,
            new JsonSerializerSettings {
                ContractResolver = new CamelCasePropertyNamesContractResolver()
            });
        return new HttpResponseMessage(HttpStatusCode.OK) {
            Content = new StringContent(jsonToReturn, Encoding.UTF8, "application/json")
        };
    }
```        
            
戻り値の型を、HttpResponseMessage とする。
