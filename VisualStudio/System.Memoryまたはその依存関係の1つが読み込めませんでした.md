# ファイルまたはアセンブリ 'System.Memory'またはその依存関係の 1 つが読み込めませんでした のエラー

今まで Visual Studio 2017を使って開発していたASP.NET MVCのアプリをVisual Studio 2019 に移行し、デバッグ実行したら、以下のエラーが発生

```
ファイルまたはアセンブリ 'System.Memory'、またはその依存関係の 1 つが読み込めませんでした。
見つかったアセンブリのマニフェスト定義はアセンブリ参照に一致しません。 (HRESULT からの例外:0x80131040)
```

原因不明

こんなページが見つかった。

https://developercommunity.visualstudio.com/content/problem/620823/systemmemorydll-version-mismatch-in-visual-studio.html

たしかに、System.Memory の 4.0.1.1 を参照しているのに、bin フォルダには、4.0.1.0 がコピーされている。
これは、Visual Studio のバグかな？

このため、ビルドアクションで強制的に System.Memory の 4.0.1.1 をコピーするようにして対処。


