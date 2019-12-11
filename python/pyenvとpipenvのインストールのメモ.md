# pyenvとpipenvのインストールのメモ

```sh
$ brew install pyenv
Updating Homebrew...
```

しばらくしたら、

```
Error: pyenv 1.2.2 is already installed
To upgrade to 1.2.9, run `brew upgrade pyenv`
```

と出たので、

```sh
$ brew upgrade pyenv
```

とコマンドを投入。

次に、

```sh
$ brew install pipenv
```

で、pipenvをインストール

```sh
$ sudo vi ~/.bash_profile
```

で、ファイル `~/.bash_profile` に以下の2行を追加

```sh
export PIPENV_VENV_IN_PROJECT=true
eval "$(pipenv --completion)"
```

以下のコマンドで、~/.bash_profile を実行し、環境を再設定。

```sh
$ source ~/.bash_profile
```

pipenvが動作するか確認する。

```sh
$ pipenv
```

ディレクトリ作成し、移動後、

```sh
$ pipenv shell
```

python --version でpythonのバージョンを確認。

```sh
(pysample) bash-3.2$ python --version
Python 3.7.3
(pysample) bash-3.2$ 
```

つまり、Python3の環境は、Python 3.7.3 ということ。

別のバージョンのPython使う方法は、明日以降。
