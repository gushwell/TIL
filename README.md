# TIL: Today I Learned by gushwell

今日学んだことをメモしています。忘れていて再度調べたものなども含んでいます。

Gushwell's Site : [Qiita](https://qiita.com/gushwell) / [GitHub](https://github.com/gushwell) もよろしく。


## Table of Contents

- [Categories](#categories)
 
  - [ASP.NET Core](#asp-net-core)
  - [ASP.NET MVC](#asp-net-mvc)
  - [.Net Core](#dotnet-core)
  - [Entity Framework Core](#ef-core)
  - [IIS](#iis)
  - [SQL Server](#sqlserver)
  - [Visual Studio](#vs)
  - [Visual Studio Code](#vscode)
  - [Microsoft Azure](#azure)
  - [Git/GitHub/GitLab](#git)
  - [python](#python)
  - [JavaScript](#js)
  - [Docker](#docker)
  - [tools](#tools)  
  - [GmoPayment](#gmopayment)
  - [other](#other)
 
  
<a id="categories"></a>
## Categories

<a id="asp-net-core"></a>
### ASP.NET Core

- [ApiVersionAttribute属性](ASP.NETCore/ApiVersionAttribute.md)
- [JWT対応](ASP.NETCore/JWT対応.md)
- [PostmanでCould_not_get_any_response.md](ASP.NETCore/PostmanでCould_not_get_any_response.md)
- [Swaggerが使えない](ASP.NETCore/Swaggerが使えない.md)
- [URLを小文字にするには](ASP.NETCore/URLを小文字にする.md)
- [クロスオリジン要求 (CORS) を有効にする](ASP.NETCore/クロスオリジン要求(CORS)を有効にする.md)
- [Web APIでルーティング指定](ASP.NETCore/WebAPIでルーティング指定.md)

<a id="asp-net-mvc"></a>
### ASP.NET MVC

- [セッションステートに使われるDBの接続文字列](ASP.NETMVC/セッションステートに使われるDBの接続文字列.md)
- [単体テストでSystem.InvalidOperationException例外発生](ASP.NETMVC/単体テストでSystem.InvalidOperationException.md)
- [EmailAddressAttributeの検証が緩すぎる](ASP.NETMVC/EmailAddressAttributeの検証が緩すぎる.md)

<a id="dotnet-core"></a>
### .NET Core

- [.NET Coreで PDFSharpを使う](DotNetCore/PDFSharp.md)
- [String.Substringの不満.md](DotNetCore/Substringの不満.md)
- [internalメソッドをテストする](DotNetCore/internalメソッドをテストする.md)

<a id="ef-core"></a>
### Entity Framework Core

- [InMemoryDatabaseは、Keyを自動インクリメントしない](EntityFrameworkCore/InMemoryDatabaseは、Keyを自動インクリメントしない.md)
- [PostgrSQLで RowVersion と同等のものを使う](EntityFrameworkCore/PostgreSQLでConcurrencyToken.md)
- [テーブル名、カラム名をsnake case に変更する](EntityFrameworkCore/PostgreSQLでsnakecase.md)
- [PostgreSQL のインストール](EntityFrameworkCore/PostgreSQLインストール.md)
- [複数のDBがある場合のMigration](EntityFrameworkCore/複数のDBがある場合のMigration.md)

<a id="iis"></a>
### IIS

- [IISで http を https にリダイレクトするには](IIS/httpsにリダイレクトする.md)
- [IISでただいまメンテナンス中ですを表示する](IIS/ただいまメンテナンス中ですを表示する.md)
- [IIS Expressでサブドメイン付きのlocalhostにアクセスする](IIS/IIS_Expressでサブドメイン付きのlocalhostにアクセスする.md)
- [webサーバーiis_expressに接続できませんでしたの対応](IIS/webサーバーiis_expressに接続できませんでしたの対応.md)
<a id="sqlserver"></a>
### SQL Server

- [SQL Serverの認証モードを変更するには](SQLServer/認証モードを変更する.md)

<a id="vs"></a>
### Visual Studio

- [Studioの .editorconfig ファイルで書式を統一](VisualStudio/editorconfigファイルで書式を統一.md) 
- [ファイルまたはアセンブリ 'System.Memory'またはその依存関係の 1 つが読み込めませんでした のエラー](VisualStudio/System.Memoryまたはその依存関係の1つが読み込めませんでした.md)
- [NuGetパッケージをローカルネットワークに公開する](VisualStudio/NuGetパッケージをローカルネットワークに公開する.md)
- [NugetパッケージのパッケージソースをComputerLevelで登録する](VisualStudio/NugetパッケージのパッケージソースをComputerLevelで登録する.md)

<a id="vscode"></a>
### Visual Studio Code

- [gitbashでAzureのazコマンドを使う時のメモ](VSCode/gitbashでazコマンド.md)

<a id="azure"></a>
### Microsoft Azure

- [Azure CLI のインストール.md](Azure/Azure_CLIのインストール.md)
- [CLIでサブスクリプションを切り替える](Azure/CLIでサブスクリプションを切り替える.md)
- [ubuntuのVMを作成する際のメモ](Azure/ubuntuのVMを作成する際のメモ.md)


<a id="git"></a>
### Git / GitHub / GitLab

- [Git メモ](git/gitメモ.md)
- [GitLabの通知をChromeで受け取る方法](git/GitLabの通知をChromeで受け取る方法.md)
- [TortoiseGitで別のマージツールを使いたい](git/TortoiseGitで別のマージツールを使いたい.md)
- [VS2019でC#のリポジトリをGitHubに新規作成する](git/VS2019でリポジトリをGitHubに新規作成する.md)
- [GitLabで緊急でバグ修正した内容をmasterとdevelopブランチに反映させたい場合の手順](git/緊急でバグ修正した内容をmasterとdevelopブランチに反映させたい.md)
- [Gitでユーザ名を指定してcloneする](git/Gitでユーザ名を指定してcloneする.md)
<a id="python"></a>
### Python

- [Macでpipenv --python 3.6 で失敗した時のメモ](python/Macでpipenv_python_3.6で失敗した時のメモ.md)
- [macでanacondaを完全削除のメモ](python/macでanacondaを完全削除のメモ.md)
- [pythonのインストールからpandas,matplotlib をインストールするまで](python/python_pandas_matplotlibをインストールするまで.md)
- [pyenvとpipenvのインストールのメモ.md](python/pyenvとpipenvのインストールのメモ.md)
- [指定した文字種だけで組み立てられてた文字列かを調べる](python/指定した文字種だけで組み立てられてた文字列かを調べる.md)
- [pipenvでmatplotlibをインストール](python/pipenvでmatplotlibをインストール.md)

<a id="js"></a>
### JavaScript

- [fetch_APIでJSONを受け取る](JavaScript/fetch_APIでJSONを受け取る.md)
- [ページが閉じるときのイベントでAjax通信](JavaScript/ページが閉じるときのイベントでAjax通信.md)

<a id="docker"></a>
### Docker

- [Docker for Windowsのインストール](Docker/Docker_for_Windowsのインストール.md)

<a id="tools"></a>
### Tools

- [Windows10のOpenSSH で接続する](tools/Windows10のOpenSSHを使う.md)
- [Postmanに関する情報](tools/postman.md)

<a id="gmopayment"></a>
### GmoPayment

- [GMOペイメントのテスト環境の APIのURL](GmoPayment/テスト環境.md)


<a id="other"></a>
### Other

- [CIDR 表記とは](other/CIDR.md)
- [OpenJDK 11.0.2 をインストールする場合の手順](other/OpenJDK11のインストール.md)
- [WindowsサーバーにChromeをインストールする方法](other/WindowsServerにChromeをインストール.md)
- [hostsファイルの変更が反映されない場合の対処](other/hostsファイルの変更が反映されない場合の対処.md)

