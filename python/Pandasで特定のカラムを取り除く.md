# Pandasで特定のカラムと取り除く


```py
df2 = p(['col1', 'col2', 'col3'], axis=1)
```

axis=1 は、カラムを削除する意味。0 にすれば、行の削除になる。

上のコードでは、col1, col2, col3 が削除される。
なお、元の DataFrameは変更されない。

