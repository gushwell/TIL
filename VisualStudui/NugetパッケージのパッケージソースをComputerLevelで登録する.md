# NugetパッケージのパッケージソースをComputerLevelで登録する

`C:\Program Files (x86)\NuGet\Config\` フォルダに `Nuget.config`ファイルを作成する。

例えば、`\\common\nuget\packages` に設定したい場合の内容は以下の通り。


```xml
<?xml version="1.0" encoding="utf-8"?>
<configuration>
    <packageSources>
        <add key="My Package Source" value="\\common\nuget\packages" />
    </packageSources>
</configuration>
```

ファイル作成には、管理者権限が必要。


`\\common\nuget\packages` に Nugetパッケージ(拡張子 nupkg)ファイルを入れるだけで良い。
Nugetパッケージのファイル名には、バージョン番号が含まれているので、複数のバージョンを入れて置ける。

