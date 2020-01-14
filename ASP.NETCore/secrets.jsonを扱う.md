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


`env.IsDevelopment()` がfalse の場合にも、secrets.jsonを利用したいのならば、以下のように、AddUserSecretsメソッドを呼び出す。

```cs
    if (env.IsDevelopment())
    {
        ...
    } 
    else
    {
        builder.AddUserSecrets<Startup>();
    }
```    
    
