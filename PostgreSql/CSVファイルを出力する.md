1. 管理者権限でコマンドプロンプトを起動

2. psql を起動

    ```
    > psql -U <username> -d {database name} -h {host name}
    ```
    
3. パスワード入力

4. 以下のコマンドを実行

    ```
    => \COPY (select * from <tablename> where <条件>) TO '<ファイル名>' WITH CSV DELIMITER ',';
    ```
    
