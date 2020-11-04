# PostGreSQLで実行計画を確認する

SQLの前に、EXPLAIN をつければ良い。

```sql
EXPLAIN SELECT part_id, update_time, creation_time, part_name, brand_id
	FROM public.exampledb
	WHERE part_code LIKE 'XE9362%'
```

以下のような結果が得られる

```
"Gather  (cost=1000.00..520190.87 rows=1651 width=651)"
"  Workers Planned: 2"
"  ->  Parallel Seq Scan on parts  (cost=0.00..519025.77 rows=688 width=651)"
"        Filter: ((part_code)::text ~~ 'XE9362%'::text)"
```
