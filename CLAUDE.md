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
| `_config.yml` | Jekyll 設定、SEO プラグイン |
| `llms.txt` | LLM 向けサイト情報 |
| `robots.txt` | クローラー設定 |

## デザイン方針

- シンプル、装飾は最小限
- 本文フォント: Courier New
- 見出し（h1）フォント: Noto Sans JP, weight 400
- テキスト色: #434343
- リンク色（SNS等）: #006580
- 大学名リンク色: 本文と同じ #434343

## 注意事項

- サイトの内容（index.md）を変更した場合は `llms.txt` も同期して更新すること
- `index.md` は純粋な Markdown で記述する（HTML タグを使わない方針）
- SNS リンク部分のみ `<div class="social-links">` で囲んでいる（リンク色の区別のため）
