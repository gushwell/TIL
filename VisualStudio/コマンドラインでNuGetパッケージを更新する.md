# NuGet CLI を使用して NuGet パッケージを更新する

Visual Studioのパッケージの復元が失敗する場合がある。このような時は、CLIを使うとうまくいく場合がある。


MySolution.sln のすべてのパッケージを現在のディレクトリに復元するには、次のコマンドを実行します。

```
nuget restore MySolution.sln
```




