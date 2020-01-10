# Pandasで指定したカラムの値を変更する

```py
     df['col1'] = df['col1'].map(lambda x: True if x == 't' else False)
```     

上のコードは、col1 の 't' を Trueに、それ以外を False に設定しなおしている。

再代入する必要がある。
