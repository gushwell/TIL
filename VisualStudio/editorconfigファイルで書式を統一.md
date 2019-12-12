# Visual Studioの .editorconfig ファイルで書式を統一

Solution Items フォルダの下に、.editorconfig ファイルを作成し、
以下のように記述することで、K&Rっぽい書式にできる。


```
[*]
end_of_line = crlf

[*.cs]
csharp_new_line_before_catch = false
csharp_new_line_before_else = false
csharp_new_line_before_finally = false
csharp_new_line_before_members_in_anonymous_types = false
csharp_new_line_before_members_in_object_initializers = false
csharp_new_line_before_open_brace = none
csharp_style_var_for_built_in_types =true:suggestion
csharp_style_var_when_type_is_apparent = true:suggestion
csharp_style_var_elsewhere = true:silent

[*.xml]
indent_style = space
```

なお、EditorConfig Language Service 拡張機能をインストールすることで、
インテリセンスが機能するようになる。

これで、ソリューションごとにスタイルを変更することも可能（やらないけど）
