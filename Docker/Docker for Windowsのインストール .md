# Docker for Windowsのインストール手順

1. BIOSで仮想化を有効にする。
	僕のPCの場合は、PC起動時に、F1キーで BIOS設定画面にすることができる。

2. Hyper-Vの有効化
	コントロールパネルの「Windows の機能の有効化または無効化]」でHyper-VとContainerを有効にする

3. Docker for Windows をダウンロード
	以下のサイトからDocker for Windows をダウンロードし、インストールする。
	https://www.docker.com/

	なお、ダウンロードするには、ユーザ登録をする必要がある。  
	ログイン後、「Get  started with Docker Desktop」ボタンをクリックし、  
	ダウンロードページで、「Download Docker Desktop for Windows」をクリックする。

4. Docker for Windows をインストール
	Docker for Windows Installer.exe  を起動し、インストールする。  
	途中のチェックボックスは、チェックしてもしなくても良い。  
	Dockerを有効にするには、PCを再起動する必要がある。  

5.  Docker Hub にログインする
	PC起動時に、Dockerが自動で起動される。  
	この時、最初の起動時に、ログイン画面が表示されるので、ここでログインする

6.  Docker起動確認

	以下の3つのコマンドを入力。エラーがでないことを確認する

	```
	docker version
	```

	```
	docker-compose -v
	```
	
	```sh
	docker run hello-world
	```

	



     
 
