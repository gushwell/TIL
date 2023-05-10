以下のように EnableRetryOnFailure を記述することで、リトライが可能になる。

```cs
services.AddDbContext<CatalogContext>(options =>　{
    options.UseSqlServer(Configuration["ConnectionString"],
    sqlServerOptionsAction: sqlOptions =>　{
        sqlOptions.EnableRetryOnFailure(
            maxRetryCount: 10,
            maxRetryDelay: TimeSpan.FromSeconds(30),
            errorNumbersToAdd: null);
    });
});
```
