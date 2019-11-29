
## PostgreSQL のインストール

以下のサイトから Windows x86-64 版をインストール

https://www.enterprisedb.com/downloads/postgres-postgresql-downloads

Version は、11.6 を選択。 （現在、Azureでサポートされているバージョンが11までのため）


ダウンロードしたら、postgresql-11.6-1-windows-x64.exe をクリックしてインストールする。
デフォルト設定のまま、インストールする。
ただし、スタックビルダーはインストールしない。

ポートは 5432 
local: deafult local

なお、スーパーユーザーは、 postgresql

GUIツールである **pgAdmin** もインストールされる。

## .NET Core用パッケージのインストール

Nugetで、次のパッケージをインストール (今回インストールしたのは、Ver3.0.1)
```
Npgsql.EntityFrameworkCore.PostgreSQL
```

## postgresql.conf を編集

以下のファイルを開く

"C:\Program Files\PostgreSQL\11\data\postgresql.conf"

この中の

```
lc_messages = 'Japanese_Japan.932'			# locale for system error message
```

を以下のように変更する。（英語にする）

```
lc_messages = 'C'
```
