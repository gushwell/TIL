# Azure AppServiceのタイムゾーンを設定するには


1. Azure ポータルの App Service サブスクリプションで、 [アプリケーション設定] メニューに移動します。
2. [アプリ設定] で次の設定を追加します。
3. Key = WEBSITE_TIME_ZONE
4. Value = 目的のタイム ゾーン
5. [保存] を選択します。

日本時間に設定するには、

- Windows: Tokyo Standard Time
- Linux: 	Asia/Tokyo

とする。
