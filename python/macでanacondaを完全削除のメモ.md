# anaconda の削除

まず、anaconda-cleanをインストール

```sh
$ conda install anaconda-clean
```

```sh
Proceed ([y]/n)? y
```

と聞いてくるので、yを選択


その後、以下のコマンドで,起動しようとした。

```sh
$ anaconda-clean
```

が、コマンドが見つからないと起動できない。

```sh
pyenv: anaconda-clean: command not found

The `anaconda-clean' command exists in these Python versions:
  anaconda3-4.3.1
```  

ということで、

```sh
$ pyenv global anaconda3-4.3.1
```


のあと、再度、コマンド投入。

```sh
$ anaconda-clean
```

いくつか、削除して良いか聞いてくるので、全て`y`で削除


そのあと、/Anaconda3フォルダを削除するらしいのですが、
僕の環境だとそのフォルダがありません。

/Users/<username>/.pyenv/ に、anacondaの環境があるみたいです。
このあたり、pythonの環境周りがよくわかっていないです。

なので、.pyenvフォルダごと削除、

その後、

```sh
sudo vim ~/.bash_profile
```

で、.pyenvに関する行を削除して保存。

最後に、

アプリケーションフォルダから、Anaconda-Navigator.appを削除

これで、全て削除できたと思います。

確認のため、pythonを起動

```sh
$ python
Python 2.7.15 (default, Aug  4 2018, 17:19:05) 
[GCC 4.2.1 Compatible Apple LLVM 9.1.0 (clang-902.0.39.2)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
```

Mac組み込みのPython環境になった。

たぶん、これで削除できたと思います。

