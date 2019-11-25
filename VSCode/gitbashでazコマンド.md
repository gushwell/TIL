拡張機能のAzure Accountを使って、azureにloginして、Bash in Cloud Shell を開こうとしたが、ターミナルには何も表示されない。

いろいろ試してみたけど、現象は変わらない。

ネットで検索すると似たような現象で困っている人もいるようだけど、解決策は見当たらない。

仕方がなにので、以下の対応を採ることにする

1. Path に Azure関連のディレクトリを標準で追加
2. bashsrcに、aliasを追加  
    ```alias az='az.cmd'```
 
3. setting.json に以下を追加  
    ``` "terminal.integrated.shell.windows": "C:\\Program Files\\Git\\bin\\bash.exe",```


これで、ターミナルを開けば、bashが起動し、azコマンドも利用できるようになった。

でも、なぜかわからないが、この後、再度、Bash in Cloud Shell を開いたら、問題なく動くようになった。
うーん、意味が分からない。


