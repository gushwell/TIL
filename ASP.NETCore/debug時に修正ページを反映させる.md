# debug時に修正ページを反映させる

ASP.NET MVC の時は、デバッグ時に、cshtmlを修正し、ページをリロードすれば、その変更が反映されたのだけど、ASP.NET Coreではこれが動作しない。

対応するには、`Microsoft.AspNetCore.Mvc.Razor.RuntimeCompilation` パッケージを入れ、
Startup.csで 以下のように`AddRazorRuntimeCompilation()`を呼び出すようにすればOK.

```cs
    public void ConfigureServices(IServiceCollection services) {
        services.AddRazorPages().AddRazorRuntimeCompilation(); 
    }
```        
