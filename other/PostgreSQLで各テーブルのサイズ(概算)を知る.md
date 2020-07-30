# PostgreSQLで各テーブルのサイズ(推測値)を知る

以下のSQLで知ることができる。あくまでも推測値。

```sql
SELECT relname, reltuples, relpages/128 as sizemb FROM pg_class ORDER BY sizemb DESC;
```

pg_classのテーブルのrelpages(ブロック数)、reltuples(行数)で知ることが可能。  


参考URL  
https://www.postgresql.jp/document/9.3/html/catalog-pg-class.html  
https://qiita.com/awakia/items/99c3d114aa16099e825d

ブロックサイズは、
```
SHOW block_size;
```
で知ることができる。
僕の環境では、8192byteだったので、`8192/(1024*1024) = 1/128` で128で割って求めている。
