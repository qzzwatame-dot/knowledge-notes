# Knowledge Notes Agent Guide

このリポジトリは、個人用の日本語知識ノートサイトです。Codexは、ユーザーから「質問：」で始まる依頼を受けた場合、調査結果を図解つきHTML記事として追加します。

## 基本方針

- 静的なHTML、CSS、必要最小限のJavaScriptだけを使う。
- フレームワーク、ビルド処理、外部ライブラリは追加しない。
- スマートフォンで読みやすく、長文に集中できる控えめなデザインを保つ。
- APIキー、パスワード、メールアドレス、住所、電話番号、個人情報をHTMLやGitに保存しない。
- 秘密情報らしきものを検出した場合は、作業を停止してユーザーに報告する。
- 著作物を大量転載しない。必要な引用は短くし、参照URLを明記する。
- 調査結果に不確実性がある場合は断定しない。

## ディレクトリ

- `technology/`: 技術、ソフトウェア、インフラ、セキュリティ
- `finance/`: 投資、金融商品、企業財務
- `economics/`: 経済、統計、政策、マクロ動向
- `job-hunting/`: 転職、面接、職務経歴、採用市場
- `ai-projects/`: AI活用、Codex、ChatGPT、個人開発
- `life/`: 生活、学習、健康、意思決定
- `assets/`: 画像などの静的アセット
- `styles/site.css`: 共通CSS

## 「質問：」を受け取った場合の手順

1. 質問の論点を整理する。
2. 必要に応じてWebを調査する。
3. 可能な限り公式資料、一次情報、論文、統計を優先する。
4. 事実と推測を明確に分ける。
5. 初心者にも理解できる日本語で説明する。
6. 具体例、比較表、因果関係の図解を入れる。
7. 必要に応じてSVGまたはCSSで図を作る。
8. 内容に最も近いカテゴリへ新しいHTML記事を保存する。
9. ファイル名は半角英数字のkebab-caseにする。
10. `index.html`の`articles`配列の先頭に記事情報を追加する。
11. 記事末尾に参考資料、URL、確認日を記載する。
12. 作成後にリンク切れ、HTML構文、スマートフォン表示を確認する。
13. 変更内容をユーザーに要約する。
14. ユーザーが差分を確認するまで、勝手に`git push`しない。
15. 承認された場合のみコミットとプッシュを行う。

## 記事HTMLの基本構成

各記事は次の構成を基本にする。

- タイトル
- 30秒で分かる要約
- なぜこの疑問が重要なのか
- 基本的な仕組み
- 図解
- 具体例
- よくある誤解
- 現実にはどう使えるか
- さらに考えたい論点
- 参考資料

## 記事テンプレート

```html
<!doctype html>
<html lang="ja">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="color-scheme" content="light dark">
  <title>記事タイトル | Knowledge Notes</title>
  <meta name="description" content="記事の短い概要。">
  <link rel="stylesheet" href="../styles/site.css">
</head>
<body class="article-page">
  <header class="article-header">
    <div class="article-body">
      <a class="back-link" href="../index.html">← トップページへ戻る</a>
      <p class="eyebrow">カテゴリ名 / YYYY-MM-DD</p>
      <h1>記事タイトル</h1>
      <p class="lead">記事の短い概要。</p>
    </div>
  </header>

  <main class="article-body">
    <section class="summary-box">
      <h2>30秒で分かる要約</h2>
      <ul>
        <li>要点1</li>
        <li>要点2</li>
        <li>要点3</li>
      </ul>
    </section>

    <section>
      <h2>なぜこの疑問が重要なのか</h2>
      <p>本文。</p>
    </section>

    <section>
      <h2>基本的な仕組み</h2>
      <p>本文。</p>
    </section>

    <section>
      <h2>図解</h2>
      <svg class="diagram" viewBox="0 0 720 320" role="img" aria-labelledby="diagram-title">
        <title id="diagram-title">図解の説明</title>
      </svg>
    </section>

    <section>
      <h2>具体例</h2>
      <p>本文。</p>
    </section>

    <section>
      <h2>よくある誤解</h2>
      <p>本文。</p>
    </section>

    <section>
      <h2>現実にはどう使えるか</h2>
      <p>本文。</p>
    </section>

    <section>
      <h2>さらに考えたい論点</h2>
      <p>本文。</p>
    </section>

    <section>
      <h2>参考資料</h2>
      <ul>
        <li><a href="https://example.com/">資料名</a>、確認日：YYYY-MM-DD</li>
      </ul>
    </section>
  </main>
</body>
</html>
```

## 品質確認

- `index.html`から追加記事へリンクできること。
- 記事から`../index.html`へ戻れること。
- スマートフォン幅で文字がはみ出さないこと。
- 参考資料URLが開けること。
- HTML構文エラーがないこと。
- 秘密情報や個人情報が含まれていないこと。
