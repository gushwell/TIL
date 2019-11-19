フォルダを作成し、そのフォルダに移動後、

```bash
$ pipenv --python 3.6
```

でmacにpython 3.6をインストールししようとして失敗。

‘X11/Xlib.h’ file not found 

のエラーになってしまう。確かにこのファイルがどこにも無い。
 
AppStoreからXCodeを更新してみる。

Homebrew自身もアップデートしてみる。

```bash
$ brew update 
```

再度、

```bash
$ pipenv --python 3.6
```

しかし、現象は変わらず。

次にやったのは、[XQuartz](https://www.xquartz.org/)からXQuartzをインストール

それから、

```bash
$ export C_INCLUDE_PATH=/usr/X11/include/X11
$ pipenv --python 3.6
```

これで、成功かと思ったら、今度は、

```con
zlib not available
```

のエラーが..

```bash
$ brew install zlib
```

で、zlib入れたけど、治らない。

で、次に試したのが、

```sh
$ xcode-select --install
sudo installer -pkg /Library/Developer/CommandLineTools/Packages/macOS_SDK_headers_for_macOS_10.14.pkg -target /
```

これで、

```bash
$ pipenv --python 3.6
```

して、やっと成功。

ちなみに、Visual Studio Code では、

```bash
$ pipenv shell
```

しなくても、デバッグができる。

```py
import sys

print(sys.version)
```

を動かしたら、

```
3.6.8 (default, Apr 18 2019, 09:00:23) 
```

と表示された。
