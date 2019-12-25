# JsonデータからC#のクラスを作成する

1. Json データをクリップボードにコピーする

2. Visual Studio の [編集]-[形式を選択して貼り付け]-[JSONをクラスとして貼り付け] を選ぶ。


例
```json
{
    "title": "星を継ぐもの3",
    "author": "ジェイムズ・P・ホーガン",
    "publishedYear": 1977,
    "id": 25
}
```

作成された C#のクラス

```c#
   public class Rootobject {
        public string title { get; set; }
        public string author { get; set; }
        public int publishedYear { get; set; }
        public int id { get; set; }
    }
```

これを元に、クラス名などを変更すればOK.

配列などにも対応してくれる。
