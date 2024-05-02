# SELECT INNER JOINで見つかった行を削除したい

## 動機

以下のSQLで見つかった行を削除したい

```sql
SELECT a
FROM my_table_a AS a
INNER JOIN my_table_b AS b ON a.id = b.id
WHERE b.my_name = "xyz"
```

## DeleteでInner joinが使えるRDBでは

以下のSQLで削除できるRDBもある。

```sql
DELETE a 
FROM my_table_a AS a
INNER JOIN my_table_b AS p ON v.oem_part_id = p.part_id 
WHERE b.my_name = "xyz"
```

PostgreSQLではこのSQLは文法エラーになる。

## 解決策1

```sql
DELETE FROM my_table_a 
WHERE id IN (
  SELECT id FROM my_table_b WHERE my_name = "xyz"
);
```

## 解決策2

```sql
delete 
from my_table_a a  
using my_table_b b 
where a.id = b.id AND b.my_name = "xyz";
```

データ量が多い場合は、解決策2の方がベター。


