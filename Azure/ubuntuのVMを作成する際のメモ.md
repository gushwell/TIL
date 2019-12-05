# Azureで、Ubuntu VMを作成する際のメモ

Linux VMを作成する際は、SSHキーが必要になる。


## SSHキーを作成する

1. Bash を起動 （ここでは、Git Bashを利用している)

2. 以下のコマンドでSSHキーを作成
```
$ ssh-keygen -t rsa -b 2048
```
以下のメッセージが出るので、Enterを押す。

```
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/idei-hideyuki/.ssh/id_rsa):
```

3. すでに存在している場合は、以下のメッセージが出るので、n を押す。

```
/c/Users/idei-hideyuki/.ssh/id_rsa already exists.
Overwrite (y/n)? n
```

4. 公開鍵を確認する

以下のコマンドで確認する

```
$ cat ./.ssh/id_rsa.pub
```

以下が表示される。

```
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDGRgox4IhX0/B2amE/Qk0dPXTn0SotpUxGnK/pa0VQMSGo/kso8cEGPNLPnebp4BbcuBqw6eD6iA6kKTnzdpxxTybvMrBNjWnY/SUG/HSrlKlORoj0KDjD2ZOagQmWraUGUUEve/NUR4nh6vgsfKkOaNbZ78e7J3kudZDfs83MCCQ7DiXkaVuQL/7YfhmYV1u+YCOAx429vRXjqMYNoJgbgTMjZfLM6Dy6AzlKA/0OXjLJcNuINWBolde2574o8Ty6CoHi72dbhZcz+8D4N2wumVSEuN6mLe+CsDlAnYgV6p1mgQWfj5QCknt8xY+N5laSkW1laULhIIEe3/ShONdP idei-hideyuki@IDEI-PC
```

5. ちなみに、公開鍵があるかどうかを調べるには、以下のコマンドを使う。

```
$ ls -al ~/.ssh
```

デフォルトでは、公開鍵のファイル名は以下のいずれかです:
```
id_dsa.pub
id_ecdsa.pub
id_ed25519.pub
id_rsa.pub
```

## VMに接続する

AzureでVMを作成したら、VMに接続してみる。

1. Azureポータルで、作成したVMのページを開き、画面上部の「接続」を選択する。

2. ページ右側に、接続の情報が表示される。

3. [VM ローカル アカウントを使用してログインする] に、接続コマンドが表示されるので、コピーボタンをクリックして、このコマンドをコピーしする。

4. Bash で、コピーしたコマンドをペーストして、SSH 接続する。

```
ssh azureuser@10.111.12.123
```
