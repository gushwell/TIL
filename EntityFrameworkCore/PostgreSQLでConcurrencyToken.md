## PostgrSQLで RowVersion と同等のものを使う

もし、Blogテーブルで、コンカレンシーチェックを行いたければ、以下のように書くだけのようだ。

```C#
protected override void OnModelCreating(ModelBuilder modelBuilder)
    => modelBuilder.Entity<Blog>()
                   .UseXminAsConcurrencyToken();
```                   


PostgreSQLには、見えない、xmin というカラムがあって、これを RowVersion カラムの代わりに使えるようになる。
そのためのカラムを定義する必要はないみたいだ。

以下の公式ページに書いてある。

https://www.npgsql.org/efcore/modeling/concurrency.html
