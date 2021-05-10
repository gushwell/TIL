1. プロジェクトを作成

2. 　パッケージをインストール
    
    ````
    Microsoft.EntityFrameworkCore.SqlServer.Design
    Npgsql.EntityFrameworkCore.PostgreSQL
    ````
    
3. 開発者用コンソールをプロジェクトのフォルダで開く。

4. 以下のコマンドを実行

    ```
    dotnet ef dbcontext scaffold "Server=myserver.example.com;Database=exampledb;Port=5432;User Id=myid;Password=password;" Npgsql.EntityFrameworkCore.PostgreSQL -o Models
    ```

5. ModelsフォルダにEntityクラスが生成される。

6. DbContextクラスは作成されないので自分で定義する。


