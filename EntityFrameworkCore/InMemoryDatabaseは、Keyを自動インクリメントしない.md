# InMemoryDatabaseは、Keyを自動インクリメントしない

タイトルの通りです。

以下のように書いても、InMemoryDatabaseの場合は、`DatabaseGenerated(DatabaseGeneratedOption.Identity)`は有効にはなりません。

```c#
        [Key]
        [DatabaseGenerated(DatabaseGeneratedOption.Identity)]
        public int Id { get; set; }
```        

単体テストを書く場合に使われることが目的にため、RDBの動作を、そのままエミュレーションしない設計思想のようです。

