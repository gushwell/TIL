C#のSubStringって、以下のコードで例外が発生しちゃうんだよね。

```
var s = "1234567890";
Console.WriteLine(s.Substring(0, 20));
```

例外が発生しないメソッドって標準で用意されていないのかな？

```
Console.WriteLine(new string(s.Take(20).ToArray()));
```

と書けばOKだけど、なんだかなー？

気が向いたら、拡張メソッドでも書く。
