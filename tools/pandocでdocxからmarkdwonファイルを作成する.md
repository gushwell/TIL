# pandocでdocxからmarkdwonファイルを作成する

mysample.docx の場合

```
pandoc mysample.docx -t markdown-raw_html-native_divs-native_spans -o mysample.md 
```

イメージファイルがある場合は、mysample.docx を mysample.zip にリネームして、zipファイルを展開する。
展開した中に、イメージファイルが格納されている。

これを手動で、作成されたmdファイルの中を見て、ディレクトリが一致するようにファイルを配置する。


