## IISで http を https にリダイレクトするには

以下のサイトから、 IIS の URL Rewrite モジュールをインストールする必要がある。

```
https://www.iis.net/downloads/microsoft/url-rewrite
```

web.configで以下を記述する。

```
<system.webServer>
  <rewrite>
    <rules>
      <clear />
      <rule name="RedirectToHttps" stopProcessing="true">
        <match url="(.*)" />
        <conditions logicalGrouping="MatchAll" trackAllCaptures="false">
          <add input="{HTTPS}" pattern="off" ignoreCase="true" />
        </conditions>
        <action type="Redirect" url="https://{HTTP_HOST}{REQUEST_URI}" redirectType="Permanent" />
      </rule>
    </rules>
  </rewrite>
</system.webServer>
```
