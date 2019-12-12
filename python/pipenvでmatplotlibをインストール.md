# pipenv で matplotlib をインストール

## Python 3.6.8 をインストール

Pythonの本家サイトからPython 3.6.8 をインストール

なお、最新の Python3.7だと、matplotlib へのインストールが失敗してしまうので、
Python3.7をアンインストールし、Python 3.6.8 をインストールしなおした。

matplotlib へのインストール失敗が、Python3.7のせいなのかが、わからずじまい。

Pythonのバージョンを確認

```
$ python --version
Python 3.6.8
```


## pipenv をインストール

```
$ pip install pipenv
```

以下のワーニングが出る。

```
Successfully installed certifi-2019.6.16 pipenv-2018.11.26 virtualenv-16.6.1 virtualenv-clone-0.5.3
You are using pip version 18.1, however version 19.1.1 is available.
You should consider upgrading via the 'python -m pip install --upgrade pip' command.
```

なので、pip を新しくする

```
$ python -m pip install --upgrade pip
```

それぞれのバージョンを確かめてみる。

```
$ pip --version
pip 19.1.1 from c:\python\python36\lib\site-packages\pip (python 3.6)
$ pipenv --version
pipenv, version 2018.11.26
```

## pipenv install

フォルダを作成し、以下のコマンドを投入。

```
$ pipenv install
$ pipenv shell
```



## numpy インストール

```
$ pipenv install numpy
```


## pandas をインストール

```
$ pipenv install pandas
```

## matplotlib をインストール

```
$ pipenv install matplotlib
```
```
