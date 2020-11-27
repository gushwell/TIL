# C#のコード分析違反をnamespace全体で抑制する

Visual Studio 2019から Scopeに、`namespaceanddescendants`が加わった。

例えば、GlobalSuppressions.csに以下のように書けば、Zead.Example と そのすべての子孫のnamespaceで`CA1801`の警告を抑制します。

```cs
[assembly: SuppressMessage("Usage", "CA1801:使用されていないパラメーターの確認",
           Scope = "namespaceanddescendants", Target = "Zead.Example")]
```



