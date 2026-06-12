# Knowledge Notes

個人用の日本語知識ノートサイトです。iPhoneのChatGPTアプリからCodexに「質問：」で始まる疑問を送ると、調査結果を図解つきのHTML記事として蓄積し、スマートフォンから読み返せる運用を想定しています。

## 構成

```text
knowledge-notes/
├── index.html
├── styles/site.css
├── assets/
├── technology/
├── finance/
├── economics/
├── job-hunting/
├── ai-projects/
├── life/
├── AGENTS.md
├── README.md
└── .gitignore
```

## ローカルで表示する

ビルド処理は不要です。次のどちらかで確認できます。

```bash
open index.html
```

または、ローカルサーバーで表示します。

```bash
python3 -m http.server 8000
```

ブラウザで `http://localhost:8000/` を開きます。

## 記事を追加する運用

Codexに次のように依頼します。

```text
質問：知りたいことを書く
```

Codexは、`AGENTS.md`のルールに従って調査し、最も近いカテゴリにHTML記事を保存し、`index.html`の記事一覧へ追加します。

## GitHubリポジトリを作成する

初回のみGitリポジトリを作成します。

```bash
git init
git add .
git commit -m "Create knowledge notes site"
```

GitHubで空のリポジトリを作成したあと、表示されたURLを使って接続します。

```bash
git branch -M main
git remote add origin https://github.com/USER/REPOSITORY.git
git push -u origin main
```

`USER`と`REPOSITORY`は自分のGitHubアカウント名とリポジトリ名に置き換えてください。

## GitHub Pagesで公開する

1. GitHubのリポジトリ画面を開く。
2. `Settings` → `Pages` を開く。
3. `Build and deployment` の `Source` で `Deploy from a branch` を選ぶ。
4. `Branch` で `main` と `/ (root)` を選び、`Save` する。
5. 数分後に表示されるURLへアクセスする。

公開前に、HTMLに秘密情報や個人情報が含まれていないか確認してください。

## 安全上の注意

- APIキー、パスワード、メールアドレス、住所、電話番号、個人情報は保存しないでください。
- 公開して問題があるメモはGitHub Pagesへ公開しないでください。
- 調査記事には参照資料と確認日を残してください。
