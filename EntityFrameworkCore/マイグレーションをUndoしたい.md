# EF CoreでマイグレーションをUndoしたい

## database updateしたのを戻したい

<previos_migramtion_name> の状態まで戻す。

```
dotnet ef database update <previos_migramtion_name>
```


## マイグレーションで生成したソースを戻したい

```
dotnet ef migrations remove
```
