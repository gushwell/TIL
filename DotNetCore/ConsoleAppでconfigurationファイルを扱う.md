# ConsoleAppでconfigurationファイルを扱う

## NuGet パッケージのインストール

```
Microsoft.Extensions.Configuration
Microsoft.Extensions.Configuration.FileExtensions
Microsoft.Extensions.Configuration.Json
```

## 準備

以下のようなメソッドを定義

```c#
    IConfiguration GetConfiguration(string relativepath, string basepath = null) {
        var configBuilder = new ConfigurationBuilder();
        configBuilder.SetBasePath(basepath ?? Directory.GetCurrentDirectory());
        configBuilder.AddJsonFile(relativepath);
        return configBuilder.Build();
    }
```

jsonファイルを準備。appconfig.json という名前で保存。

```json
{
  "AppSettings": {
    "MaxFileSize": 5000
  }
}
```

## 情報を取得する

これは、カレントディレクトリにある appconfig.json から値を取得するコード。

```
    var config = GetConfiguration("appconfig.json");
    var size = config["AppSettings:MaxFileSize"];
    Console.WriteLine(size);
```            
