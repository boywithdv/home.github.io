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

## 画像の使用方法

### 画像ファイルの配置
1. プロジェクトルートに`images`フォルダを作成
2. 画像ファイルを`images`フォルダに配置
3. 推奨ファイル形式：`.jpg`, `.png`, `.webp`

### 画像の種類と用途

#### プロジェクト画像
- ファイル名例：`fitness-app.jpg`, `todo-app.jpg`
- 推奨サイズ：600×400px以上
- 用途：プロジェクトカードの表示画像

#### プロフィール画像
- ファイル名：`profile.jpg`
- 推奨サイズ：300×300px以上（正方形）
- 用途：Aboutセクションのプロフィール写真

#### 背景画像（オプション）
- ファイル名例：`hero-bg.jpg`
- 推奨サイズ：1920×1080px以上
- 用途：ヒーローセクションの背景

### HTMLでの画像表示
```html
<!-- プロジェクト画像 -->
<div class="project-image">
    <img src="images/project-name.jpg" alt="プロジェクト説明" />
</div>

<!-- プロフィール画像 -->
<div class="profile-image">
    <img src="images/profile.jpg" alt="プロフィール写真" />
</div>
```

### CSSでの背景画像
```css
.hero {
    background-image: url('images/hero-bg.jpg');
    background-size: cover;
    background-position: center;
}
```

### 画像最適化のヒント
1. ファイルサイズを抑える（500KB以下推奨）
2. WebP形式を使用すると軽量化可能
3. レスポンシブ対応のため複数サイズを用意

### 画像がない場合
画像ファイルが見つからない場合は、プレースホルダー（🖼️）が表示されます。

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

### 1. GitHubリポジトリの作成
1. GitHubにログイン
2. 右上の「+」ボタン → 「New repository」をクリック
3. Repository nameを`あなたのGitHubユーザー名.github.io`として作成
   - 例：GitHubのユーザー名が「john-doe」の場合 → `john-doe.github.io`
4. 「Public」を選択
5. 「Create repository」をクリック

### 2. ローカルリポジトリの初期化と接続
```bash
# 現在のディレクトリでGitを初期化
git init

# リモートリポジトリを追加
git remote add origin https://github.com/boywithdv/home.github.io.git

# mainブランチを作成
git branch -M main
```

### 3. ファイルをGitHubにプッシュ
```bash
# 変更をステージング
git add .

# コミット
git commit -m "Initial commit"

# GitHubにプッシュ
git push -u origin main
```

### 4. デプロイの確認
1. GitHubのリポジトリページに移動
2. 「Settings」タブをクリック
3. 左サイドバーの「Pages」をクリック
4. 「GitHub Pages」セクションで、サイトが公開されていることを確認
   - `https://boywithdv.github.io/home.github.io` でアクセス可能
   - デプロイには数分かかる場合があります

### 5. 更新方法
サイトを更新する場合は、以下のコマンドを実行：
```bash
git add .
git commit -m "更新内容の説明"
git push origin main
```

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
