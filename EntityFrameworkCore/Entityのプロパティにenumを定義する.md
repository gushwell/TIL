# Entityのプロパティにenumを定義する

## enum の定義

例えば

```cs
    public enum SampleEnum {
        MyValue1,
        MyValue2,
        MyValue3
    }
```

## Entity クラス

```cs
public class MySample {
    public SampleEnum SampleEnum { get; set; }
    ...
}
```

## DbConextクラス

```cs
       protected override void OnModelCreating(ModelBuilder modelBuilder) {
            // enum との変換
            modelBuilder
                .Entity<MySample>()
                .Property(e => e.SampleEnum)
                .HasConversion<int>();
...
```

`.HasConversion<int>()` を `.HasConversion<string>()` にすれば、文字列に変換することもできる。
