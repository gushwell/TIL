1. 管理者権限でコマンドプロンプトを起動

2. psql を起動

```
 > psql -U <username> -d {database name} -h {host name}
```

3. パスワード入力

4. 以下のコマンドを実行
```
  => \copy <tablename> from 'ファイルパス' with csv
```  

5. psqlを終了

```
  => \q
```  
