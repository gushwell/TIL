# Azure CLIで、複数のサブスクリプションの中からアクティブなサブスクリプションを変更する


以下のコマンドで、サブスクリプションの一覧を表示させる。

```
az account list --output table
```

表示された一覧からサブスクリプションの名前を確認し、以下のコマンドで切り替える。


```
az account set --subscription "My Demos"
```

ここでは、"My Demos" というサブスクリプションに切り替えている。
