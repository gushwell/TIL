# 文字列をN文字ずつに分割する方法


2つの方法を示す。3文字ずつ分割する例。

### Matchesを使う

```cs
string str = "123456789123456789";
var strs = Regex.Matches(str, @"(.{1,3})")
    .Cast<Match>()
    .Select(x => x.Value)
    .ToArray();
Console.WriteLine(string.Join('|', strs));
```

最長一致なので、`{1,3}`で通常は3文字と一致する。最後のあまりは、1文字でも2文字でも一致する。


### Splitを使う。

```cs
string str = "123456789123456789";
var strs = Regex.Split(str, @"(?<=\G.{3})(?!$)");
Console.WriteLine(string.Join('|', strs));
```

正規表現のアンカーという機能を使って分割している。



