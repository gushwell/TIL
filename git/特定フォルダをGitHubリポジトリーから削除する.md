ここでは、myfloderを削除する例を示す。


### 1. .gitignore に myfloder/ を追加

まず、今後誤ってコミットしないように .gitignore に以下を追加。

```
myfolder/
```

すでに追加されていればこのステップはスキップしてOK。

### 2. Git のキャッシュから myfolder を削除

```
git rm -r --cached myfolder
```

--cached を付けることで、ローカルのファイルは削除せず、Git の追跡対象からのみ削除。

### 3. 削除をコミット

```
git commit -m "Remove myfolder folder from repository"
```

### 4. GitHub にプッシュ

```
git push origin main
```

ブランチ名が main でない場合は適宜読み替え。