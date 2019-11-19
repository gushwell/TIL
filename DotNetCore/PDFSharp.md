## PDFsharpNetStandard2

.NET Core で、PDFSharpを使うには、"PDFsharpNetStandard2" を Nuget から取得。

あとは、.NET Framework と同様の方法で、PDFを出力すればOK.

名前空間名も変更なし。そのまま同じものが利用できる。

ただし、ソースは非公開。

System.Drawing.Common.dll に依存している。

## PdfSharpCore

NuGetにはないが、

[https://github.com/ststeiger/PdfSharpCore](https://github.com/ststeiger/PdfSharpCore)

には、ソースが公開された派生 pdfsharp が存在する。
こちらは、namespaceが異なるが、クラスは互換性がある。

IFontResolver を実装すれば、日本語も扱える。

こちらは、System.Drawing.Common.dll に依存していない。
代わりに、[SixLabors.Core](https://github.com/SixLabors/Core) を利用。
