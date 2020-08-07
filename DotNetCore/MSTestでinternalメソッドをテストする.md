# MSTestで、internalクラス、internalメソッドをテストする。

AssemblyInfo.csに、以下の属性を付加する。

```cs
using System.Reflection;
using System.Runtime.CompilerServices;
using System.Runtime.InteropServices;

[assembly: InternalsVisibleTo("MyAppTests")]
```

こうすることで、MyAppTestsアセンブリだけに、internalクラス、メソッドが公開される。

なお、AssemblyInfo.csである必要はないが、これまでの経緯から、AssemblyInfo.cs　が良いかなという程度。

