# tsclientはリモートデスクトップの接続元コンピュータを指す


"tsclient"は、特別なコンピュータ名で、リモートデスクトップの接続元のコンピュータを表している。

"tsclient"は、Terminal Server Client を意味している。


例えば、コマンドプロンプトで、

```
dir \\tsclient\C\Users\gushwell\source
```

などとすれば、自分のPC(接続元PC)の以下のディレクトリのファイル一覧を取得することができる。


```
C\Users\gushwell\source
```


なお、cdコマンドで、カレントディレクトリに移動することはできないようだ。
