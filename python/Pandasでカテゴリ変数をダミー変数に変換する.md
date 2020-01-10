# Pandasでカテゴリ変数をダミー変数に変換する

機械学習させるときの前処理で利用できる


```py
import pandas as pd
...
df2 = pd.get_dummies(df, columns=["product", "mtype"])
```

columns で指定したカラムがカテゴリ値を格納する変数。

