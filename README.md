# ポートフォリオウェブサイト

このリポジトリは、GitHub Pagesでホストされる個人ポートフォリオウェブサイトのソースコードです。

## 起動方法

### 1. 初回セットアップ

```bash
# リポジトリをクローン
git clone https://github.com/xxx/xxx.github.io.git

# プロジェクトディレクトリに移動
cd xxx.github.io
```

### 2. ローカルサーバーの起動

以下のいずれかの方法でローカルサーバーを起動できます：

```bash
# 方法1: Python 3を使用（推奨）
python3 -m http.server 8000

# 方法2: Python 2を使用
python -m SimpleHTTPServer 8000

# 方法3: npxを使用
npx http-server
```

### 3. ウェブサイトへのアクセス

ローカルサーバー起動後、以下のURLでアクセスできます：

- メインURL: http://localhost:8000
- 代替URL: http://127.0.0.1:8000

### 4. サーバーの停止方法

サーバーを停止するには、ターミナルで`Ctrl + C`を押します。

## 機能

- レスポンシブデザイン
- モダンなUI/UXデザイン
- スムーズスクロール
- コンタクトフォーム
- プロジェクト表示セクション
- スキルセクション
- ソーシャルメディアリンク

## 技術スタック

- HTML5
- CSS3
- JavaScript (Vanilla)
- Font Awesome (アイコン)

## カスタマイズ方法

### 内容の変更

1. `index.html`を編集して以下の項目を変更:
   - 自己紹介文
   - プロジェクト内容
   - スキルセット
   - ソーシャルメディアリンク

### デザインの変更

1. `css/styles.css`の`:root`セクションで色を変更:
```css
:root {
    --primary-color: #2563eb;    /* メインカラー */
    --secondary-color: #1e40af;  /* サブカラー */
    --text-color: #1f2937;       /* テキストカラー */
    --background-color: #ffffff; /* 背景色 */
    --section-bg: #f3f4f6;       /* セクション背景色 */
}
```

## トラブルシューティング

### よくある問題と解決方法

1. **サーバーが起動しない場合**
   - ポート8000が他のプロセスで使用されていないか確認
   - 別のポート番号を試す（例：`python3 -m http.server 8080`）

2. **ページが表示されない場合**
   - ブラウザのキャッシュをクリア
   - 別のブラウザで試す
   - `index.html`が正しい場所にあるか確認

3. **スタイルが適用されない場合**
   - ブラウザの開発者ツールでエラーを確認
   - CSSファイルのパスが正しいか確認
   - `styles.css`が`css`フォルダ内にあるか確認

## GitHub Pagesでの公開方法

1. GitHubで`[username].github.io`という名前の新しいリポジトリを作成

2. ローカルリポジトリをGitHubにプッシュ
```bash
git add .
git commit -m "Initial commit"
git push origin main
```

3. 数分後に`https://[username].github.io`でサイトが公開されます

## コンタクトフォームの設定

現在のコンタクトフォームはデモ用です。実際に機能させるには以下のサービスとの連携をお勧めします：

- Formspree
- Netlify Forms
- Google Forms

## 開発環境のセットアップ（オプション）

より快適な開発のために、以下のツールの使用をお勧めします：

1. **VSCode拡張機能**
   - Live Server
   - HTML CSS Support
   - JavaScript (ES6) code snippets

2. **ブラウザ開発者ツール**
   - Chrome DevTools
   - Firefox Developer Tools

## ライセンス

このプロジェクトはMITライセンスの下で公開されています。 