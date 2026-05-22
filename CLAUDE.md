# Project: takayuki1997.github.io

Takayuki OGI（荻 多加之）の個人サイト。Jekyll + GitHub Pages で構築。

## ワークフロー

- ファイル編集 → `git add` → `git commit` → `git push` で自動デプロイ
- GitHub Actions が Jekyll ビルドを実行し、GitHub Pages に公開される
- URL: https://takayuki1997.github.io/

## 主要ファイル

| ファイル | 役割 |
|---|---|
| `index.md` | サイトのコンテンツ（Markdown） |
| `_layouts/default.html` | HTML の枠組み、Analytics、フォント読み込み |
| `assets/css/style.css` | デザイン（CSS） |
| `_config.yml` | Jekyll 設定。`jekyll-seo-tag`（メタタグ生成）と `jekyll-sitemap`（サイトマップ生成）を有効化 |
| `favicon.svg` | ファビコン（SVG、#434343 の四角に白字 T） |
| `favicon.png` | ファビコン PNG フォールバック（Safari 用） |
| `llms.txt` | LLM 向けサイト情報 |
| `robots.txt` | クローラー設定 |
| `Gemfile` | Jekyll プラグインの依存関係（`jekyll-seo-tag`、`jekyll-sitemap`） |
| `assets/images/qrcode.png` | サイト URL の QR コード。サイトには表示しない個人用アセット（スライド資料用） |

## デザイン方針

- シンプル、装飾は最小限
- 本文フォント: Courier New
- 見出し（h1）フォント: Noto Sans JP, weight 400
- テキスト色: #434343
- リンク色（デフォルト）: #006580
- 大学名リンク色: `.affiliations` クラスで本文と同じ #434343 に上書き
- 連絡先リンク色: `.contact` クラスで薄いグレー #888 に上書き（控えめにする意図）
- 行間: body の `line-height: 1.6` を基本とし、リスト項目（`li`）は `line-height: 1.0`（折り返し時の詰め）
- リスト間隔は `margin-bottom` で制御（`line-height` に依存しない）

## HTML 構造

- 所属一覧: `<div class="affiliations">` 内の `<ul>` リスト
- SNS リンク: `<div class="social-links">` 内の `<ul>` リスト
- 連絡先: `<div class="contact">` 内の `<ul>` リストにメール（mailto）リンクをページ最下部に配置
- div タグには `markdown="1"` を付けて Kramdown に Markdown 処理させる
- `<title>` タグは自前で定義し、`{% seo title=false %}` でプラグインのタイトル出力を抑制
- サイト言語: `lang="en"`（コンテンツが英語のため）

## 注意事項

- サイトの内容（index.md）を変更した場合は `llms.txt` も同期して更新すること
- `index.md` は基本 Markdown で記述する（div タグはクラス付与のためのみ使用）
- Google Search Console に登録済み（オーナー: takayuki1997@gmail.com、所有権確認は GA `G-VC3N3802VM` 経由）。`_config.yml` で sitemap プラグインを外すと sitemap.xml が消えて Search Console 側で「取得できませんでした」になるので注意
