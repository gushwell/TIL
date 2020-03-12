# PostgreSQLでpostgresのパスワードをリセットする

Windows 10 + PostgreSQL11 での例

## 1. pg_hba.conf の編集

以下のフォルダ の pg_hba.conf を開く
```
C:\Program Files\PostgreSQL\11\data
```

ファイルの最後のほうに次のような記述がある。このmd5 を trust に変更して保存する。

```
# TYPE  DATABASE        USER            ADDRESS                 METHOD

# IPv4 local connections:
host    all             all             127.0.0.1/32            md5
# IPv6 local connections:
host    all             all             ::1/128                 md5
# Allow replication connections from localhost, by a user with the
# replication privilege.
host    replication     all             127.0.0.1/32            md5
host    replication     all             ::1/128                 md5
```

## 2. PostgreSQLにサービスを再起動する

サービス名は、`postgresql-x64-11`  
これをタスクマネージャから再起動する。


## 3. パスワードを変更する

コマンドプロンプトを開き、psql.exeがインストールされているフォルダに移動する。

以下のコマンドを起動

```
> psql -U postgres
psql (11.6)
"help" でヘルプを表示します。

postgres-# \password
新しいパスワードを入力してください: <新しいパスワード>
もう一度入力してください: <新しいパスワード>
postgres-# \q
```

## 4. pg_hba.conf を元に戻す

## 5. PostgreSQLのサービスを再起動する


