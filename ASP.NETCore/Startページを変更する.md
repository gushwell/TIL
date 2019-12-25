# スタートページを変更する

1. index.cshtml を削除する  
   これをやらないとうまくいかない。
   
2. Startup.cs で以下の記述をする

   ```cs
   public void ConfigureServices(IServiceCollection services) {
        services.AddRazorPages(options => {
            options.Conventions.AddPageRoute("/Matter/Index", "");
        }); 
    }      
   ```
   
   なお、これは Razor Pagesの場合。MVCは、AddMvcメソッドの中で同様の設定をする。
   
   
