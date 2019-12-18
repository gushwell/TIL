# ASP.NET Core でのクロスオリジン要求 (CORS) を有効にする

## クロスオリジン要求とは

通常、ブラウザでAjax通信を行う場合は、同一生成元ポリシー(Same Origin Policy)によってWebページを生成したドメイン以外へのHTTPリクエストができない。
しかし、異なるドメインにアクセスしたいというケースは多々ある。
そのために作成されたのがCORSで、CORSとはCross-Origin Resource Sharingの略である。

呼び出された側が、どこからアクセスされたものなら許可するかを指定することで、これを実現している。
実際には、ブラウザとサーバー側でHTTPヘッダを使ってアクセス制御情報をやりとりしている。


## 必要なパッケージ

Microsoft.AspNetCore.Cors

## Startup.cs

```cs
readonly string MyAllowSpecificOrigins = "_myAllowSpecificOrigins";
        
public void ConfigureServices(IServiceCollection services) {
   ...
   services.AddCors(o => o.AddPolicy(MyAllowSpecificOrigins, builder =>
   {
       builder.AllowAnyOrigin()    // すべてのオリジンからの CORS 要求を許可
              .AllowAnyMethod()    // すべての HTTP メソッドを許可
              .AllowAnyHeader();   // すべての作成者要求ヘッダーを許可
   }));
   }
```

```cs
public void Configure(IApplicationBuilder app, IWebHostEnvironment env) {
    ...
    app.UseRouting();
    app.UseCors(MyAllowSpecificOrigins);   // これを追加
    app.UseAuthorization();    
    app.UseEndpoints(endpoints => {
        endpoints.MapControllers();
    });
}
```        

AddCorsは、安全性を高めるために、以下のように特定のオリジンだけを許可することもできる。

```cs
    services.AddCors(options =>
    {
        options.AddPolicy(MyAllowSpecificOrigins,
        builder =>
        {
            builder.WithOrigins("http://example.com",
                                "http://www.contoso.com")
                   .AllowAnyMethod();
        });
    });
```    
