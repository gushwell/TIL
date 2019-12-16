# IIS Express で サブドメイン付きのlocalhostにアクセスする方法

hosts ファイルに記述

```
127.0.0.1       sub1.localhost
127.0.0.1       sub2.localhost
```

ソリューションフォルダの .vs フォルダの下にある aookicationhost.config を変更

```
        <bindings>
          <binding protocol="http" bindingInformation="*:51769:localhost" />
          <binding protocol="https" bindingInformation="*:44311:localhost" />
          <binding protocol="http" bindingInformation="*:51769:sub1.localhost" />
          <binding protocol="https" bindingInformation="*:44311:sub1.localhost" />
          <binding protocol="http" bindingInformation="*:51769:sub2.localhost" />
          <binding protocol="https" bindingInformation="*:44311:sub2.localhost" />
        </bindings>
```

Visual Studio 2019 を管理者権限で起動。

プロジェクトをデバッグ。
