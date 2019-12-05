# Windows10のOpenSSH で接続する

Windows10には、標準でSSHクライアントソフトが入っている。それを使う方法。

`C:\Users\<username>\.ssh`  に configファイルを作成。

以下、そのサンプル
```
host myposgre
	user zeadadmin
	hostname 10.5.12.208
	port 22
	identityfile ~/.ssh/id_rsa
```

複数のエントリを記入しておけば、接続先を名前で指定することができる。

以下のコマンドで、SSH接続ができる。

```
> ssh myposgre
```


## OPenSSHがインストールされているかを確認するには、

コマンドプロンプトで、以下をタイプ

```
where ssh
```

以下が表示されていれば、OK.

```
C:¥Windows¥System32¥OpenSSH¥ssh.exe
```

git for windows の ssh.exeが見つかった場合は、PATHの順番で、優先順位を変更する。
