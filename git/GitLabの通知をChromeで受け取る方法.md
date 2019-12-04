# GitLab の通知をChromeで受け取る方法

1.  Chrome拡張機能の `GitLab Notifier for Google Chrome` をインストールします。

2. Chrome のアドレスバーの横に、GitLab Notifier for Google Chrome  のアイコンが表示されるので、右クリックし、オプションを選びます。

3.  GitLab Setting に以下を入力します。

     GitLab Path: https://gitlab.com/
     GitLab API Path: https://gitlab.com/api/v4
     Private token: GitLabで取得したtoken （後述）

4. Save ボタンを押します。

5.  Refresh Repository List ボタンをクリックします。

6. プロジェクトの一覧が表示されますので、参加しているプロジェクトで通知を受けたいものにチェックを付けます。  

7. 下の Save ボタンを押します。

これで、Chrome で通知を受け取ることが可能になります。

# GitLabの personal access token を取得する

1. 自分のIDでGitLab へログインします

2. 右上の自分のアイコンをクリックし、「設定」を選びます。

3. 左側のメニュー一覧から「アクセストークン」を選びます。

4.  名前を半角英字で入力します。（名前を自由に決めてOK）

5.  `api` にチェックを入れます。

6.  `Create personal access token` ボタンを押します。

7.  生成されたトークンをメモします。

このトークン文字列は後から見ることができないみたい。

探したけどわからなかった。

なので、必ずメモを取っておく必要がある。


