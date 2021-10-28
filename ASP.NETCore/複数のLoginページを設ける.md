# ASP.NET Coreで、複数のログインページを設ける。

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

```
[Authorize]
```

参照URL:
https://stackoverflow.com/questions/48032216/implement-different-login-page-for-each-role-in-asp-net-core-2

