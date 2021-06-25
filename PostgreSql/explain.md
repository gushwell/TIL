# PostGreSQLで実行計画を確認する

SQLの前に、EXPLAIN ANALYZE をつければ良い。

```sql
EXPLAIN ANALYZE SELECT part_id, update_time, creation_time, part_name, brand_id
	FROM public.exampletable
	WHERE part_code LIKE 'XE9362%'
```

以下のような結果が得られる

```
"Index Scan using ix_parts_part_code on parts  (cost=0.56..2.59 rows=1893 width=50) (actual time=11.513..11.513 rows=0 loops=1)"
"  Index Cond: (((part_code)::text ~>=~ 'XE9362'::text) AND ((part_code)::text ~<~ 'XE9363'::text))"
"  Filter: ((part_code)::text ~~ 'XE9362%'::text)"
"Planning Time: 1.616 ms"
"Execution Time: 11.552 ms"
```
