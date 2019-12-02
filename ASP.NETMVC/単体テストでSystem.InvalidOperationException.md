ASP.NET MVCで単体テストプロジェクトを作成し、実行したら以下のエラーに遭遇。


> Message: クラス xxxxxxxxxxxxxxxxx のインスタンスを作成できません。エラー: System.InvalidOperationException: Web ワーカー プロセス (HRESULT=0x80040154) 外部へのネイティブ構成サポートを初期化できません。
nativerd.dll は %windir%\system32\inetsrv 内に配置しなければなりません。。


確かに、このDLLは存在しない。

調べたら、以下のフォルダにはある。

```
"C:\Windows\WinSxS\wow64_microsoft-windows-i..raries-servercommon_31bf3856ad364e35_10.0.17763.1_none_a4a61fc6fc98c57c\nativerd.dll"
```

```
"C:\Windows\WinSxS\amd64_microsoft-windows-i..raries-servercommon_31bf3856ad364e35_10.0.17763.1_none_9a517574c8380381\nativerd.dll"
```

これを、 %windir%\system32\inetsrv 内に配置しないといけないということだろうか？

でも、そんな対応方法はおかしいと思って、調べたところ、以下の方法で解消できました。


Windowsの機能の有効かまたは無効化で、HTTPアクティブ化にチェックを入れる。

