# SQLLocalDbを作成し直す方法

以下のコマンドを順に実行します。

```
sqllocaldb stop "MSSQLLocalDB"
sqllocaldb delete "MSSQLLocalDB"
sqllocaldb create "MSSQLLocalDB"
sqllocaldb start "MSSQLLocalDB"
```

## `sqllocaldb stop "MSSQLLocalDB"`でstopできなかった場合の対応

次のコマンドでSQLServerのプロセス一覧を表示させます。

```
PS> Get-Process -Name sqlservr
```

以下のような結果が得られます。

```
 NPM(K)    PM(M)      WS(M)     CPU(s)      Id  SI ProcessName
 ------    -----      -----     ------      --  -- -----------
     68   785.48     575.48       0.00   17476   0 sqlservr
     59   690.60     493.04       0.56   19272   1 sqlservr
```

このように、複数の`sqlservr`が起動している場合があります。
ここでIDを特定して、以下のようにIDを指定してプロセスを終了させます。

```
 Stop-Process -Id 19272 -Force
```


どちらが、該当するのかわからない場合は、どちらかのIDを指定してプロセスを終了させてみます。

これで、

```
qllocaldb info MSSQLLocalDB
```

で状態を見て、状態が停止ならばOK.ダメなら、もう片方のIDでプロセスを終了します。。
