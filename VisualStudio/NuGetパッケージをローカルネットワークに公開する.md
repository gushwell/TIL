# NuGetパッケージをローカルネットワークに公開する

ローカルネットワーク上にnugetパッケージを公開するには、以下のコマンドを使う。

```
nuget add new_package.1.0.0.nupkg -source \\myserver\packages
```

これだけ。

これで、以下のような階層構造を作成してくれる。


```
\\myserver\packages
  └─<packageID>
    └─<version>
      ├─<packageID>.<version>.nupkg
      └─<other files>
```      
