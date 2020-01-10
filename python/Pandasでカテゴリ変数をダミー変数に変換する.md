# Pandasでカテゴリ変数をダミー変数に変換する

機械学習させるときの前処理で利用できる


```py
import pandas as pd
...
df2 = pd.get_dummies(df, columns=["product", "mtype"])
```

columns で指定したカラムがカテゴリ値を格納する変数。


## category_encoders を使う方法

複数のカラムを指定できる
```py
import category_encoders as ce

    list_cols = ['seq_m_product', 'cat_create']

    # OneHotEncodeしたい列を指定。Nullや不明の場合の補完方法も指定。
    ce_ohe = ce.OneHotEncoder(cols=list_cols,handle_unknown='impute')

    # pd.DataFrameをそのまま突っ込む
    df_ce_onehot = ce_ohe.fit_transform(df)
```    

なお、scikit-learn の OneHotEncoder は、複数のカラムを指定する方法がない。
