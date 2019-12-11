# internalメソッドをテストする

- テストしたいプロジェクト : Gushwell.Example
- テストプロジェクト: Gushwell.Example.Tests

DotNetCoreのプロジェクトでは、AssemblyInfo.csが存在しないが、DotNetCoreでも、これまでと同じようにすれば、internalなメソッドをテストできる。

Gushwell.Example プロジェクトに、AssemblyInfo.csを追加する。
内容は以下の通り。

```cs
using System.Runtime.CompilerServices;
[assembly: InternalsVisibleTo("Gushwell.Example.Tests")]
```

これでOK.


