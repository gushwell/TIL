# VisualStudioでシークレットマネージャを使う

appsettings.jsonからシークレット情報を追い出す方法は以下の通り。  
ただし、この方法は、ローカルデバッグ時にのみ有効。production環境では、別の方法が必要。

1. ソリューションエクスプローラーのプロジェクトを右クリック
2. 空のsecrets.json が作成される
3. appsettings.jsonと同じ書式で、シークレット情報を記述する。

これだけ。

ただし、Program.csで、以下のように、 `Host.CreateDefaultBuilder(args)`を呼び出していることが前提。


```cs
public static IHostBuilder CreateHostBuilder(string[] args) =>
    Host.CreateDefaultBuilder(args)
        .ConfigureWebHostDefaults(webBuilder =>
        {
            webBuilder.UseStartup<Startup>();
        });
```        

なお、ファイルの場所は以下の通り。

```
%APPDATA%\Microsoft\UserSecrets\<user_secrets_id>\secrets.json
```

<user_secrets_id>は、.csprojファイルの内をみると確認できる。


```xml
  <PropertyGroup>
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ...
    <UserSecretsId>b43978a9-27c3-4282-b731-f5b8e0614c35</UserSecretsId>
  </PropertyGroup>
```  
