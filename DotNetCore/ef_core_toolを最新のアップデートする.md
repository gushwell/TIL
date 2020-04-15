#  EF Core toolsを最新のアップデートする

dotnet コマンドを起動すると、以下のようなエラーが出る場合がある。

```
The EF Core tools version '3.1.2' is older than that of the runtime '3.1.3'. 
Update the tools for the latest features and bug fixe the latest features and bug fixes.
```

このような時は、以下のコマンドをタイプして、 EF Core tools を最新にする


```
dotnet tool update --global dotnet-ef
```
