# SQL Server Management Studio で条件に一致した行を編集したい

SQL Server Management Studio には、「Edit Top xxx Rows」のメニューから先頭の指定した行数を編集する機能がある。

これだと、後ろにある行を編集できない。以下の手順でやれば、条件に一致した行を表示して、編集できるようになる。

1. テーブルを右クリック
2. 「Edit Top xxx Rows」を選ぶ
3. 上部の「Show SQL Pane」アイコンをクリックする
4. SQLを書き換える。
5. メニュー「Query Designer」-「Execute SQL」を選ぶ

これで、クエリの結果が表示されるので、該当行を変更すればOK.
