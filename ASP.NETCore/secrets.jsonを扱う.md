# secrets.jsonを扱う

## secrets.sjonの編集

1. Visual Studio のプロジェクトを右クリックし、「ユーザシークレットの管理」を選択
2. secrets.json が開く
3. ここに、フラットな形式で、appsettingsの内容を記述する
    例:
    ```json
    {
        "Movies:ServiceApiKey": "12345",
    }
    ```

上記の操作で、以下のフォルダに secrets.jsonファイルが作成される。

#### WIndowsの場合

```
%APPDATA%\Microsoft\UserSecrets\<user_secrets_id>\secrets.json
```

#### Linux/Macの場合

```
~/.microsoft/usersecrets/<user_secrets_id>/secrets.json
```

`<user_secrets_id>`は、 .csprojファイルのropertyGroup 内に UserSecretsId 要素の値。
この値は、上記、1の操作を最初に実行した時に、設定される。

```xml
  <PropertyGroup>
    <TargetFramework>netcoreapp3.1</TargetFramework>
    <UserSecretsId2>79a3edd0-2092-40a2-a04d-dcb46d5ca9ed</UserSecretsId2>
  </PropertyGroup>
```  


## startup.cs の編集

基本は何もしなくても、デバッグ時には、secrets.sjon が利用される。
なお、program.csで、 CreateDefaultBuilder を呼び出していることが前提。


`env.IsDevelopment()` がfalse の場合にも、secrets.jsonを利用したいのならば、以下のようなコードを書く必要がある。

```cs
public Startup(IWebHostEnvironment env) {
    var builder = new ConfigurationBuilder()
        .SetBasePath(env.ContentRootPath)
        .AddJsonFile("appsettings.json",
                     optional: false,
                     reloadOnChange: true)
        .AddEnvironmentVariables();

    if (env.IsDevelopment()) {
        ...
    }
    else { 
        ...
    }

    builder.AddUserSecrets<Startup>();
    Configuration = builder.Build();
}
```    

デフォルトでは、開発環境時のみsecrets.jsonが利用される構成になっていることから、これは、運用環境での利用は推奨されていないのかもしれない。

開発環境と運用環境とで同じシークレット情報を利用する場合は、appsettings.jsonにシークレット情報を保存しないようにするために、この機能が必要になりそう。
GITのソース管理対象にはシークレット情報を入れない運用にするには、この機能が必要。

運用時は、環境変数から取得。開発時は、secrets.jsonから取得。というスタイルが良いのか？
