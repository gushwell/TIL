# Postman の Could not get any response のエラーを解決するには

ASP.NET Core でWebAPIを作成し、Postmanで接続したところ以下のエラーで通信できない。

以下の URLに解決策が書いてある。

https://knkomko.hatenablog.com/entry/2019/10/02/001032

簡単に書くと、以下のことをやればよい。

1. POstmanの File - Settings - General を選択
2. SSL certificate verification を OFF にする

