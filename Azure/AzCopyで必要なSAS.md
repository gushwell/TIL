# AzCopyで必要なSAS

[https://docs.microsoft.com/ja-jp/azure/storage/blobs/storage-blob-user-delegation-sas-create-cli](https://docs.microsoft.com/ja-jp/azure/storage/blobs/storage-blob-user-delegation-sas-create-cli)

によれば、以下のようなコマンドで作成できるとあるが、

```
az storage container generate-sas \
    --account-name <storage-account> \
    --name <container> \
    --permissions acdlrw \
    --expiry <date-time> \
    --auth-mode login \
    --as-user
```

これで作成したSASを使って、azCopyを行おうとすると、認証エラーでコピーができない。

AzureのポータルサイトでもSASを作成することができる。
なぜか、こちらで作成したSASを使うと、無事コピーができる。

理由は不明。

以下のようなコマンドで、ファイルをローカルにダウンロードできた。

```
azcopy copy "https://mystorageaccount.file.core.windows.net/myfileshare/myTextFile.txt?sv=2018-03-28&ss=bjqt&srs=sco&sp=rjklhjup&se=2019-05-10T04:37:48Z&st=2019-05-09T20:37:48Z&spr=https&sig=%2FSOVEFfsKDqRry4bk3qz1vAQFwY5DDzp2%2B%2F3Eykf%2FJLs%3D" "C:\myDirectory\myTextFile.txt"
```

? 以降がSAS

なお、WIndows環境では、' ではなく、"でパスを括る。
