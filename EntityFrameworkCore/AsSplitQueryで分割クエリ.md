# AsSplitQueryメソッドでクエリを分割する

Include, ThenIncludeを使ったクエリは、デフォルトでは単一クエリが有効になっています。

## クエリ単位で分割クエリを有効にする

AsSplitQuery()メソッドを使えば、特定のクエリを複数の SQL クエリに "分割" するように指定できます。JOIN ではなく、含まれているコレクション ナビゲーションごとに追加の SQL クエリが生成されます。

この機能は、EF Core 5.0 以降で有効です。

```cs
 var blogs = context.Blogs
        .Include(blog => blog.Posts)
        .AsSplitQuery()
        .ToList();
```

## グローバルで分割クエリを有効にする

以下のようなコードを書くことでグローバルで分割クエリを有効にできます。

```cs
protected override void OnConfiguring(DbContextOptionsBuilder optionsBuilder)
{
    optionsBuilder
        .UseSqlServer(
            @"Server=(localdb)\mssqllocaldb;Database=EFQuerying;Trusted_Connection=True",
            o => o.UseQuerySplittingBehavior(QuerySplittingBehavior.SplitQuery));
}
```

分割クエリが既定値として構成されている場合でも、AsSingleQuery()メソッドを使えば、特定のクエリを単一のクエリとして実行できます。

```cs
using (var context = new SplitQueriesBloggingContext())
{
    var blogs = context.Blogs
        .Include(blog => blog.Posts)
        .AsSingleQuery()
        .ToList();
}
```
