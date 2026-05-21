# takayuki1997.github.io

Takayuki OGI（荻 多加之）の個人サイトです。

- URL: https://takayuki1997.github.io/

## このサイトの仕組み

GitHub だけで無料で公開できるウェブサイトです。サーバー契約や独自ドメイン購入は不要で、必要なのは GitHub アカウントだけです。

### GitHub Pages

[GitHub Pages](https://pages.github.com/) は、GitHub が提供する無料の静的サイトホスティングサービスです。リポジトリにファイルを置くだけで、自動的に Web で公開されます。

リポジトリ名を `<username>.github.io` にすると、URL は `https://<username>.github.io/` になります。このリポジトリは `takayuki1997.github.io` という名前なので、URL は https://takayuki1997.github.io/ です。

### Jekyll

[Jekyll](https://jekyllrb.com/) は静的サイトジェネレータです。Markdown で書いたコンテンツを HTML に変換してくれます。GitHub Pages は Jekyll をネイティブサポートしているので、追加設定なしで利用できます。

このサイトでは:

- 本文は `index.md`（Markdown）
- ページの枠組みは `_layouts/default.html`（HTML テンプレート）
- デザインは `assets/css/style.css`
- サイト全体の設定は `_config.yml`

これらを Jekyll が組み合わせて HTML を生成します。

## 公開フロー

1. ローカルでファイルを編集
2. `git commit` & `git push` で GitHub にアップロード
3. GitHub Actions が Jekyll ビルドを実行
4. 数十秒〜1分で公開 URL に反映

SSH や FTP でサーバーにアップロードする必要はなく、`git push` だけで更新できます。

## ファイル構成

| ファイル | 役割 |
|---|---|
| `index.md` | サイトのコンテンツ（Markdown） |
| `_layouts/default.html` | HTML の枠組み（Analytics、フォント読み込みなど） |
| `assets/css/style.css` | デザイン（CSS） |
| `_config.yml` | Jekyll 設定 |
| `favicon.svg` / `favicon.png` | ファビコン |
| `llms.txt` | LLM 向けのサイト情報 |
| `robots.txt` | クローラー設定 |
| `Gemfile` | Jekyll プラグインの依存関係 |

## コスト

完全無料です。GitHub アカウントを持っていればすぐに始められます。

独自ドメイン（例: `example.com`）を使いたい場合はドメイン取得費用（年 1,000〜2,000円程度）が別途かかりますが、`<username>.github.io` のままなら一切費用はかかりません。

## 自分でも作ってみたい人へ

このリポジトリは Public なので、自由に参考にしてください。

実際このサイトは AI コーディングアシスタント [Claude Code](https://claude.ai/code) で作成・更新しています。HTML や CSS の知識がなくても、対話するだけで構築・更新できます。

1. GitHub アカウントを作成
2. `<your-username>.github.io` という名前で新しいリポジトリを作成し、ローカルにクローン
3. Claude Code を起動して「Jekyll + GitHub Pages で個人サイトを作って」と依頼
4. 内容やデザインを対話で調整（「もっとシンプルに」「メールリンクを追加して」など）
5. リポジトリ設定の Pages から GitHub Pages を有効化
6. Claude Code に commit & push を依頼すれば公開

もちろん、Web 技術に慣れている方は手動でファイルを編集しても構いません。

## License

[MIT License](LICENSE) — このサイトの仕組みやコードは自由に利用できます。
