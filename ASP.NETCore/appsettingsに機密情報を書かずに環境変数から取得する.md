# appsettingsに機密情報を書かずに環境変数から取得する

## appsettings.json

appsettingsにはデバッグ時の情報を記述します。

## 環境変数の定義

本番環境では、この情報を環境変数に定義します。
例えば、


```json
  "ConnectionStrings": {
    "Movies": "Server=(localdb)\\mssqllocaldb;..."
  }
```  

上記のような定義がappsettingsにある場合は、環境変数 "ConnectionStrings__Movies" に本番環境の接続文字列を定義します。

`__` (アンダースコアを２つ連続させる)は階層構造を示すデリミタです。このデリミタは、`:`に自動的に置換されます。

## C#側の対応

通常通り、appsettings.jsonから取得するコードを書くだけです。環境変数から取得するようなコードを書く必要はありません。

なお、明示的にappsettingsから値を取得する場合は、以下のように `__` を `:` に置き換えて取得します。

```cs
_constr = Configuration["ConnectionStrings:Movies"];
```
