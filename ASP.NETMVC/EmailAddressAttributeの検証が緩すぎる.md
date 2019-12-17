# EmailAddressAttributeの検証が緩すぎるので困った

EmailAddressAttributeの検証が緩すぎるので、

yamada, taro (yamada-taro@example.com)

のような入力も通してしまいます。

これを、`System.Net.Mail.MailAddress` にそのまま渡すと例外が発生します。

System.Net.Mail.MailAddressを利用する際に、メールアドレスを抜き出すのが良いのか、

それとも、入力検証時にエラーにするほうが良いのか、悩みどころです。
