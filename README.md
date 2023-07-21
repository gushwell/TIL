# TIL: Today I Learned by gushwell

今日学んだことをメモしています。忘れていて再度調べたものなども含んでいます。

Gushwell's Site : [Qiita](https://qiita.com/gushwell) / [GitHub](https://github.com/gushwell) もよろしく。


## Table of Contents

- [Categories](#categories)
 
  - [ASP.NET Core](#asp-net-core)
  - [ASP.NET MVC](#asp-net-mvc)
  - [.NET / C#](#dotnet-core)
  - [Entity Framework Core](#ef-core)
  - [SQL Server](#sqlserver)
  - [PostgreSQL](#postgresql)
  - [Visual Studio](#vs)
  - [Visual Studio Code](#vscode)
  - [Microsoft Azure](#azure)
  - [IIS](#iis)
  - [Git/GitHub/GitLab](#git)
  - [Python](#python)
  - [JavaScript](#js)
  - [Docker](#docker)
  - [tools](#tools)  
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
- [クロスオリジン要求 (CORS) を有効にする](ASP.NETCore/クロスオリジン要求を有効にする.md)
- [debug時に修正したページ(cshtml)を反映させる](ASP.NETCore/debug時に修正ページを反映させる.md)
- [Startページを変更する](ASP.NETCore/Startページを変更する.md)
- [appsettingsに機密情報を書かずに環境変数から取得する](ASP.NETCore/appsettingsに機密情報を書かずに環境変数から取得する.md)
- [program.csでappsettings.jsonの値を取得する](ASP.NETCore/program.csでappsettings.jsonの値を取得する.md)
- [VisualStudioでシークレットマネージャを使う](/ASP.NETCore/VisualStudioでシークレットマネージャを使う.md)
- [環境(ASPNETCORE_ENVIRONMENT)がDevelopmentかどうかを判断する](ASP.NETCore/環境ASPNETCORE_ENVIRONMENTがDevelopmentかどうかを判断する.md)
- [Razor Pages: 一つのページで複数のformを使う](ASP.NETCore/一つのページで複数のformを使う.md)
- [TryValidateModelでモデルの一部だけを検証する](ASP.NETCore/TryValidateModelでモデルの一部だけを検証する.md)
- [複数のLoginページを設ける](ASP.NETCore/複数のLoginページを設ける.md)
- [Web APIでルーティング指定](ASP.NETCore/WebAPIでルーティング指定.md)
- [Web APIでhtmlを返す](ASP.NETCore/WebAPIでhtmlを返す.md)
- [Web APIでグローバルフィルターを設定する](ASP.NETCore/WebAPIでグローバルフィルターを設定する.md)
- [モデルバインドするコレクションの最大サイズを設定する](ASP.NETCore/モデルバインドするコレクションの最大サイズを設定する.md)

<a id="asp-net-mvc"></a>
### ASP.NET MVC

- [セッションステートに使われるDBの接続文字列](ASP.NETMVC/セッションステートに使われるDBの接続文字列.md)
- [単体テストでSystem.InvalidOperationException例外発生](ASP.NETMVC/単体テストでSystem.InvalidOperationException.md)
- [EmailAddressAttributeの検証が緩すぎる](ASP.NETMVC/EmailAddressAttributeの検証が緩すぎる.md)
- [シークレット情報をweb.configから切り離す](ASP.NETMVC/ASP.NET_MVCでシークレット情報をweb.configから切り離す.md)

<a id="dotnet-core"></a>
### .NET / C#

- [String.Substringの不満](DotNetCore/Substringの不満.md)
- [文字列をN文字ずつに分割する](DotNetCore/文字列をN文字ずつに分割する.md)
- [internalメソッドをテストする](DotNetCore/internalメソッドをテストする.md)
- [ConsoleAppでconfigurationファイルを扱う](DotNetCore/ConsoleAppでconfigurationファイルを扱う.md)
- [複数の書式を指定して日付文字列をParseする](DotNetCore/複数の書式指定して日付文字列をParseする.md)
- [カルチャを指定しTryParseで数値に変換したい](DotNetCore/カルチャを指定しTryParseしたい.md)
- [配列をシャッフルするコード](DotNetCore/配列をシャッフルするコード.md)
- [1970年01月01日からの経過時間を秒で求める](DotNetCore/1970年01月01日からの経過時間を秒で求める.md)
- [C#のコード分析違反をnamespace全体で抑制する](DotNetCore/コード分析違反をnamespace全体で抑制する.md)
- [EF Core toolを最新にアップデートする](DotNetCore/ef_core_toolを最新のアップデートする.md)
- [.NET Coreで PDFSharpを使う](DotNetCore/PDFSharp.md)
- [自己完結型アプリを生成](DotNetCore/自己完結型アプリを生成.md)
- [既定のホスト構成の環境変数](DotNetCore/既定のホスト構成の環境変数.md)
- [バイナリファイルを構造体に読み込む](DotNetCore/バイナリファイルを構造体に読み込む.md)
- [列挙値を重複させない設定](DotNetCore/列挙値を重複させない設定.md)
- [単体テストでappsettings.jsonを利用する](DotNetCore/単体テストでappsettings.jsonを利用する.md)

<a id="ef-core"></a>
### Entity Framework Core

- [テーブルのカラムにマッピングされないプロパティを定義する](EntityFrameworkCore/テーブルのカラムにマッピングされないプロパティを定義する.md)
- [InMemoryDatabaseは、Keyを自動インクリメントしない](EntityFrameworkCore/InMemoryDatabaseは、Keyを自動インクリメントしない.md)
- [テーブル名、カラム名をsnake case に変更する](EntityFrameworkCore/PostgreSQLでsnakecase.md)
- [テーブル名を取得する](EntityFrameworkCore/テーブル名を取得する.md)
- [プロパティに対応するカラム名を取得する](EntityFrameworkCore/プロパティに対応するカラム名を取得する.md)
- [Entityのプロパティにenumを定義する](EntityFrameworkCore/Entityのプロパティにenumを定義する.md)
- [DbContextを多段継承したい](EntityFrameworkCore/DbContextを多段継承したい.md)
- [ルール外の外部キープロパティ名をつける](EntityFrameworkCore/ルール外の外部キープロパティ名をつける.md)
- [プログラム実行時にDBマイグレーションを行う](EntityFrameworkCore/プログラム実行時にDBマイグレーションを行う.md)
- [AsSplitQueryでSQLクエリを分割する](EntityFrameworkCore/AsSplitQueryで分割クエリ.md)
- [SQL Server接続時にリトライする](EntityFrameworkCore/EF_CoreでSQL_Server接続時にリトライする.md)
- [SQLのコマンドタイムアウト値を設定する](EntityFrameworkCore/SQLのコマンドタイムアウト値を設定する.md)
- [EF_Core_toolsを更新する](EntityFrameworkCore/EF_Core_toolsを更新する.md)
- [複数のDBがある場合のMigration](EntityFrameworkCore/複数のDBがある場合のMigration.md)
- [クラスライブラリでマイグレーションしたい](EntityFrameworkCore/クラスライブラリでマイグレーション.md)
- [マイグレーションをUndoしたい](EntityFrameworkCore/マイグレーションをUndoしたい.md)
- [マイグレーションをリセットしたい](EntityFrameworkCore/マイグレーションをリセットする.md)
- [PostgrSQLで RowVersion と同等のものを使う](EntityFrameworkCore/PostgreSQLでConcurrencyToken.md)
- [PostgreSQLでsnakecaseのカラム、テーブル名を扱う](EntityFrameworkCore/PostgreSQLでsnakecase.md)
- [PostgreSQLでデータベースファースト](EntityFrameworkCore/PostgreSQLでデータベースファースト.md)

<a id="sqlserver"></a>
### SQL Server

- [SQL Serverの認証モードを変更するには](SQLServer/認証モードを変更する.md)
- [データベースのisolation_levelを確認する](SQLServer/isolation_levelを確認する.md)
- [コマンドでフルバックアップ](SQLServer/コマンドでフルバックアップ.md)
- [SQL Server ExpressでAUTO_CLOSEオプションをOFFにする](SQLServer/AUTO_CLOSEオプションをOFFにする.md)

<a id="postgresql"></a>
### PostgreSQL

- [PostgreSQLのインストール](PostgreSql/PostgreSQLインストール.md)
- [PostgreSQLでpostgresのパスワードをリセットする](PostgreSql/PostgreSQLでpostgresのパスワードをリセットする.md)
- [PostgreSQLで各テーブルのサイズ(概算)を知る](PostgreSql/PostgreSQLで各テーブルのサイズを知る.md)
- [PostgreSQLの実行計画を確認する](PostgreSql/explain.md)
- [PostgreSQLのインデックスのサイズを確認する](PostgreSql/インデックスのサイズを確認する.md)
- [PostgreSqlの全てのパラメータ値を表示する](PostgreSql/全てのパラメータ値を表示する.md)
- [psqlでSQLファイルを実行する](PostgreSql/psqlでSQLファイルを実行する.md)
- [テーブルの内容をCSVファイルに出力する](PostgreSql/CSVファイルを出力する.md)
- [CSVファイルをテーブルにインポートする](PostgreSql/CSVファイルをインポートする.md)



<a id="vs"></a>
### Visual Studio

- [Visual Studioの .editorconfig ファイルで書式を統一](VisualStudio/editorconfigファイルで書式を統一.md) 
- [ファイルまたはアセンブリ 'System.Memory'またはその依存関係の 1 つが読み込めませんでした のエラー](VisualStudio/System.Memoryまたはその依存関係の1つが読み込めませんでした.md)
- [JsonデータからC#のクラスを作成する](VisualStudio/Jsonデータからクラスを作成する.md)
- [xUnitとMoqを使う準備](VisualStudio/xUnitとMoqを使う準備.md)
- [Visual Studioでの発行で特定のファイルを除外する](VisualStudio/発行時に特定のファイルを除外する.md)
- [NuGetパッケージをローカルネットワークに公開する](VisualStudio/NuGetパッケージをローカルネットワークに公開する.md)
- [NugetパッケージのパッケージソースをComputerLevelで登録する](VisualStudio/NugetパッケージのパッケージソースをComputerLevelで登録する.md)
- [Nuget.exe自身を最新版に更新したい](VisualStudio/Nuget.exe自身を最新版に更新したい.md)
- [NuGetパッケージをCLIで更新する](VisualStudio/NuGetパッケージをCLIで更新する.md)

<a id="vscode"></a>
### Visual Studio Code

- [MacにVSCodeのPathを追加する方法](VSCode/MacにVSCodeのPathを追加する.md)
- [gitbashでAzureのazコマンドを使う時のメモ](VSCode/gitbashでazコマンド.md)
- [Pythonのflake8で特定エラーを除外する](VSCode/Pythonのflake8で特定エラーを除外する.md)
- [Pythonのフォーマットで勝手に改行しないようにする](VSCode/Pythonのフォーマットで勝手に改行しないようにする.md)

<a id="azure"></a>
### Microsoft Azure

- [Azure CLI のインストール](Azure/Azure_CLIのインストール.md)
- [CLIでサブスクリプションを切り替える](Azure/CLIでサブスクリプションを切り替える.md)
- [ubuntuのVMを作成する際のメモ](Azure/ubuntuのVMを作成する際のメモ.md)
- [Azure Functions の API バージョニング](Azure/Azure_FunctionsのAPIバージョニング.md)
- [AzureFunctionsでJSONを返す](Azure/AzureFunctionsでJSONを返す.md)
- [Azure App ServicesにPython(Flask)をデプロイする](Azure/Azure_AppServicesにPython_Flaskをデプロイする.md)
- [Azure_Key_Vaultで削除されたシークレット情報を復旧させる](Azure/Azure_Key_Vaultで削除されたシークレット情報を復旧させる.md)
- [AzCopyで必要なSAS](Azure/AzCopyで必要なSAS.md)
- [AppServiceにタイムゾーンを設定する](Azure/AppServiceにタイムゾーンを設定する.md)

<a id="iis"></a>
### IIS

- [IISで http を https にリダイレクトするには](IIS/httpsにリダイレクトする.md)
- [IISでただいまメンテナンス中ですを表示する](IIS/ただいまメンテナンス中ですを表示する.md)
- [IIS Expressでサブドメイン付きのlocalhostにアクセスする](IIS/IIS_Expressでサブドメイン付きのlocalhostにアクセスする.md)
- [webサーバーiis_expressに接続できませんでしたの対応](IIS/webサーバーiis_expressに接続できませんでしたの対応.md)


<a id="git"></a>
### Git / GitHub / GitLab

- [.NET用gitignoreファイルを作成する](/git/DotNET用gitignoreファイルを作成する.md)
- [Git メモ](git/gitメモ.md)
- [GitLabの通知をChromeで受け取る方法](git/GitLabの通知をChromeで受け取る方法.md)
- [TortoiseGitで別のマージツールを使いたい](git/TortoiseGitで別のマージツールを使いたい.md)
- [VS2019でC#のリポジトリをGitHubに新規作成する](git/VS2019でリポジトリをGitHubに新規作成する.md)
- [GitLabで緊急でバグ修正した内容をmasterとdevelopブランチに反映させたい場合の手順](git/緊急でバグ修正した内容をmasterとdevelopブランチに反映させたい.md)
- [Gitでユーザ名を指定してcloneする](git/Gitでユーザ名を指定してcloneする.md)
- [GitLabのCIでdotnet3.1のプロジェクトをビルドする](git/GitLabのCIでdotnet3.1を使う.md)
- [Gitで改行コードが自動変換される](git/改行コードが自動変換される.md)
- [リモートリポジトリから不要なフォルダを削除する](git/リモートリポジトリから不要なフォルダを削除する.md)
 

<a id="python"></a>
### Python

- [Macでpipenv --python 3.6 で失敗した時のメモ](python/Macでpipenv_python_3.6で失敗した時のメモ.md)
- [macでanacondaを完全削除のメモ](python/macでanacondaを完全削除のメモ.md)
- [pythonのインストールからpandas,matplotlib をインストールするまで](python/python_pandas_matplotlibをインストールするまで.md)
- [pyenvとpipenvのインストールのメモ](python/pyenvとpipenvのインストールのメモ.md)
- [指定した文字種だけで組み立てられてた文字列かを調べる](python/指定した文字種だけで組み立てられてた文字列かを調べる.md)
- [pipenvでmatplotlibをインストール](python/pipenvでmatplotlibをインストール.md)
- [Pandasで特定のカラムを取り除く](python/Pandasで特定のカラムを取り除く.md)
- [Pandasでカテゴリ変数をダミー変数に変換する](python/Pandasでカテゴリ変数をダミー変数に変換する.md)
- [Pandasで指定したカラムの値を変更する](python/Pandasで指定したカラムの値を変更する.md)
- [Flask で Cors の対応](python/FlaskでCorsの対応.md)
- [pipでインストール済みパッケージ確認する](python/pipでインストール済みパッケージ確認.md)

<a id="js"></a>
### JavaScript

- [fetch_APIでJSONを受け取る](JavaScript/fetch_APIでJSONを受け取る.md)
- [ページが閉じるときのイベントでAjax通信](JavaScript/ページが閉じるときのイベントでAjax通信.md)
- [ローカルにあるテキストファイルを読み込む](JavaScript/ローカルにあるテキストファイルを読み込む.md)
- [bootstrap5でモーダルダイアログを手動で開く](JavaScript/bootstrap5でモーダルダイアログを手動で開く.md)

<a id="docker"></a>
### Docker

- [Docker for Windowsのインストール](Docker/Docker_for_Windowsのインストール.md)


<a id="tools"></a>
### Tools

- [WindowsのOpenSSH で接続する](tools/Windows10のOpenSSHを使う.md)
- [scpコマンドでLinuxsサーバーのファイルをダウンロードする](tools/scpコマンドでLinuxsサーバーのファイルをダウンロードする.md)
- [Postmanに関する情報](tools/postman.md)
- [pandocでdocxからmarkdwonファイルを作成する](tools/pandocでdocxからmarkdwonファイルを作成する.md)



<a id="other"></a>
### Other

- [CIDR 表記とは](other/CIDR.md)
- [OpenJDK 11.0.2 をインストールする場合の手順](other/OpenJDK11のインストール.md)
- [WindowsサーバーにChromeをインストールする方法](other/WindowsServerにChromeをインストール.md)
- [hostsファイルの変更が反映されない場合の対処](other/hostsファイルの変更が反映されない場合の対処.md)
- [Chromeのサービスワーカーを削除する](other/Chromeのサービスワーカーを削除する.md)
- [tsclientはリモートデスクトップの接続元コンピュータを指す](other/tsclientはリモートデスクトップの接続元コンピュータを指す.md)
- [ファイルの一覧を再起的に取得する](other/ファイルの一覧を再起的に取得する.md)
- [コマンドプロンプトの文字コードを変更する.md](other/コマンドプロンプトの文字コード変更.md)
- [WSL上のUbuntuをリセットする](other/WSL上のUbuntuをリセットする.md)
- [bootstrap5のtooltipsで改行するには](other/bootstrap5のtooltipsで改行するには.md)
