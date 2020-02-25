# SQL Server：データベースのisolation levelを確認する

以下のSQLで確認可能

```
USE [<mydatabase>]
GO
DBCC USEROPTIONS
```

例えば、以下のような結果が得られる


Set Option | Value
-----------|------------
textsize |	2147483647
language |	日本語
dateformat |	ymd
datefirst |	7
lock_timeout |	-1
quoted_identifier |	SET
arithabort |	SET
ansi_null_dflt_on |	SET
ansi_warnings |	SET
ansi_padding |	SET
ansi_nulls |	SET
concat_null_yields_null |	SET
isolation level |	read committed snapshot
