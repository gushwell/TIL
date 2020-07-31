# web.configの接続文字列などを外部ファイルから読み込むようにする


## web.config

以下のように書くことで、外部ファイルから読み込める

```xml
  <connectionStrings configSource="Config\connectionStrings.config"/>
  <appSettings configSource="Config\appSettings.config"/>
```

connectionStrings、appsettingsは全体が置き換わる。一部だけを切り離すことはできない。
