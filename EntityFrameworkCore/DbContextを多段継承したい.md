# DbContextを多段継承する時のTips

<br>

## 継承元

protectedなコンストラクタを定義する。

```cs
public class BaseDbContext : DbContext {
    public BaseDbContext(DbContextOptions<BaseDbContext> options)
        : base(options) {
    }

    protected BaseDbContext(DbContextOptions options)
        : base(options) {
    }
}
```

## 派生先

継承元のBaseDbContextから派生する。

```cs
public class DelivedDbContext : BaseDbContext {
    public DelivedDbContext (DbContextOptions<DelivedDbContext> options)
        : base(options) {
    }
}
```

baseでは、protectedなコンストラクタが呼ばれる。


参考:  
https://github.com/dotnet/efcore/issues/7533#issuecomment-353669263
