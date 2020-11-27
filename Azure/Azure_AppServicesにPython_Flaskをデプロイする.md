# Azure App ServicesにPython+Flaskアプリをデプロイする

## ローカルGitリポジトリからデプロイする方法

最初は、以下のコマンドで、デプロイする

```sh
az login
az account set --subscription subscriptionname
az group create --name mygroup --location japaneast
az appservice plan create --name planname --location japaneast --is-linux --sku B2 --resource-group mygroup
az webapp create --name webappname --plan planname --runtime "PYTHON|3.7" --resource-group mygroup
az webapp deployment user set --user-name myusername --password mypassword
az webapp deployment source config-local-git --name webappname --resource-group mygroup
git remote add azure "https://myusername@webappname.scm.azurewebsites.net/webappname.git"
git add .
git commit -m 'first commit'
git push azure master
```

subscriptionname, mygroup, planname, webappname, myusername, mypassword は 自由に設定

2回目以降は、リポジトリを更新し、azureのリモートリポジトリにpushすればよい。


```sh
git push azure master
```
