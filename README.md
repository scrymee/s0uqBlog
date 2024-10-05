本ブログは、Reactベースの静的ページジェネレータGatsbyを用いて構築しています。

## 概要
以下が利点で選定。

・gatsbyのCliをNodePackageManager(npm)を利用して、読み込み使用される
・静的サイトのデプロイは時間がかかるが、ローカルの開発用サーバーで変更をすぐに確認できる
・比較的カスタマイズが容易

[The Best React-Based Framework | Gatsby](https://www.gatsbyjs.com/)

### QuickStart

[Quick Start | Gatsby](https://www.gatsbyjs.com/docs/quick-start/)


### 使用しているテンプレート

ポートフォリオ・ブログ・ヘッドレスCMSなどのテンプレートの中で、以下のブログ向けテンプレートを使用中です。

[gatsby-starter-blog | Gatsby](https://www.gatsbyjs.com/starters/gatsbyjs/gatsby-starter-blog/)

▼利点
・ブログ用のテンプレート
・Markdown利用可能

### コミット内容
・差分はContentディレクトリ配下、cssファイル、config関連のファイルのみ
　・gatsby-config.js　（テキストの編集）
　・src/components/bio.js（プロフィール文の変更）
　・src/images/profile-pic.png（画像変更）
　・src/style.css （ダークモードに変更）
　。content（記事）

・GitHubActionを使い、静的ページの生成まで行う。
当初はGithubActionで全部する予定だった。テンプレートの取り込み、package.jsonの更新、差分ファイルの更新・静的ページ生成・・・
→記事更新後に、GitHubPageに更新される時間が長くなりうるため、やめる
→Gatsbyのテンプレートをコミットして、GitHubAction上では、静的ページの生成をできるようにしている。
