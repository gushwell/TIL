# Flask で Cors の対応

## パッケージのインストール

```
flask_cors  3.0.8
```

## Python のコード

```py

...
from flask_cors import CORS
...

app = Flask(__name__)
CORS(app)

```


