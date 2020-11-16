# カルチャを指定しTryParseで数値に変換したい

以下のように現在のスレッドのカルチャを変更することができる。

```cs
Thread.CurrentThread.CurrentCulture = new CultureInfo("id_ID");
```

なお、.NET Framework 4.5.2 以前のバージョンでは、変更できない。

これで、通常のように、TryParseすれば良い。

なお、明示的に変換するには、以下のように記述する。

```cs
var style = NumberStyles.Number | NumberStyles.AllowCurrencySymbol;
if (decimal.TryParse(str, style, CultureInfo, out var num)) {
    ...
}
```

styleの値は、お好みで。

