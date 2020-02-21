# EF_Core_toolsを更新する.

`dotnet ef`コマンドで、以下のようなエラーが出る場合に対処

```
The EF Core tools version '3.1.0' is older than that of the runtime '3.1.2'. 
Update the tools for the latest features and bug fixes.
```


以下のコマンドでツールを更新する

```
dotnet tool update --global dotnet-ef
```

成功すれば、以下のメッセージが表示される

```
ツール 'dotnet-ef' がバージョン '3.1.0' からバージョン '3.1.2' に正常に更新されました。
```
