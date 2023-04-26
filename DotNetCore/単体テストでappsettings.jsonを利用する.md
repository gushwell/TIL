## 単体テストで　appsettings.jsonを利用する

ここでは、appsettings.sjonに定義してあるデータベースの接続文字列を取り出し、DbContextのインスタンスを生成する例を示す。


```cs
    [TestClass()]
    public class MyTests
    {
        private readonly IConfiguration _configuration;
        private readonly MyService _sv;
      
        public MyTests()
        {
            _configuration = new ConfigurationBuilder()
                .SetBasePath(Directory.GetCurrentDirectory())
                .AddJsonFile(@"appsettings.json", false, false)
                .AddEnvironmentVariables()
                .Build();
            var constr = _configuration.GetSection("ConnectionStrings:AppDbContext").Value;
            var contextOptions = new DbContextOptionsBuilder<AppDbContext>()
                .UseSqlServer(constr)
                .Options;

            using var db = new AppDbContext(contextOptions);
            _sv = new MyService(db);
        }

        [TestMethod()]
        public void Mytest1()
        {
          ...
        }
    }
```
