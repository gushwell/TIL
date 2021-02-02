# EF CoreでマイグレーションをUndoしたい

## database updateしたのを戻したい

```
dotnet ef database update <previos_migramtion_name>
```


## マイグレーションで生成したソースを戻したい

```
dotnet ef migrations remove
```
