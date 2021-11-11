# ASP.NET Coreで、複数のログインページを設ける。

## うまくいかなかったやり方


参照URL:
https://stackoverflow.com/questions/48032216/implement-different-login-page-for-each-role-in-asp-net-core-2


Startup.cs で以下のコードを追加

```cs
            services.AddAuthentication(options => {
                options.DefaultScheme = "UserAuth";
            })
            .AddCookie("UserAuth", options =>
            {
                options.LoginPath = "/identity/account/login";
            })
            .AddCookie("AdminAuth", options => {
                options.LoginPath = "/admin/account/Login/";
            });
```

各ページ/コントローラーでは、以下のように書く。

```
[Authorize(Roles = "Administrator", AuthenticationSchemes = "AdminAuth")]
```

```
[Authorize(Roles = "User", AuthenticationSchemes = "UserAuth")]
```

ログインページの振り分けはうまく行くのだが、Authorizeによる許可で弾かれてしまう。

## 無理やりの対応

login.cshtml.cs において、returnUrlの値を見て、どこのページにアクセスしたのかを判断し、例えば、"/admin/ で始まっていれば、
"/admin/account/Login/"　にリダイレクトするようにする。

Authorize属性は、Roleだけを指定する。

```
[Authorize(Roles = "Administrator")]
```

```
[Authorize(Roles = "User"]
```

