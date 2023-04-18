## scpコマンドでLinuxsサーバーのファイルを一括ダウンロードする方法

ターミナルで、以下のコマンドを実行する

```
scp -r <username>@<hostname>:<sorce directory> <target directory>
```

`<hostname>`は、example.com とか、192.168.xxx.xxx のようなIPアドレス。

`<source directory>` は、コピー元のディレクトリの相対パス、or　絶対パス

`<target directory>` は、コピー先の自PCのディレクトリ

例
```
scp -r gushwell@example.com::/home/mywork /temp
```
  
このコマンドを投入すると、パスワードを要求されるので、パスワードを入れると、コピーが開始される。
