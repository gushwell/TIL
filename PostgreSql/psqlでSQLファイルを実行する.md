# psqでSQLファイルを実行する


1. sqlファイルがあるディレクトリに移動する

2. psqlでログインする

```
psql -U <username> -d <database_name> -h <host_name>
```

3. パスワードを入力する

4. sqlファイルを実行する

```
# \i example.sql
```
