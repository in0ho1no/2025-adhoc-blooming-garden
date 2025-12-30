# Growing Photos - GitHub Pages公開方法

## 手順

### 1. GitHubリポジトリの作成

1. [GitHub](https://github.com)にログイン
2. 右上の「+」から「New repository」をクリック
3. リポジトリ名を入力（例：`growing-photos-game`）
4. 「Public」を選択
5. 「Create repository」をクリック

### 2. ファイルのアップロード

#### 方法A: ブラウザから直接アップロード（簡単）

1. 作成したリポジトリのページで「uploading an existing file」をクリック
2. `growing-photos.html` を `index.html` にリネームしてアップロード
3. 「Commit changes」をクリック

#### 方法B: Git コマンドを使用

```bash
# リポジトリをクローン
git clone https://github.com/YOUR_USERNAME/growing-photos-game.git
cd growing-photos-game

# ファイルをコピー（index.htmlにリネーム）
cp /path/to/growing-photos.html index.html

# コミット＆プッシュ
git add index.html
git commit -m "Add Growing Photos game"
git push origin main
```

### 3. GitHub Pagesの有効化

1. リポジトリのページで「Settings」をクリック
2. 左側のメニューから「Pages」をクリック
3. 「Source」で「Deploy from a branch」を選択
4. 「Branch」で「main」と「/ (root)」を選択
5. 「Save」をクリック

### 4. 公開完了！

数分後、以下のURLでゲームにアクセスできます：

```
https://YOUR_USERNAME.github.io/growing-photos-game/
```

## 注意事項

- ファイル名は必ず `index.html` にする必要があります
- GitHub Pagesは無料で利用できます
- 変更を加えた場合は、同じ手順でファイルを更新するだけでOKです
- HTTPSで自動的に配信されます

## カスタムドメインの設定（オプション）

独自ドメインを使いたい場合：

1. GitHub Pages設定で「Custom domain」にドメインを入力
2. DNSプロバイダーでCNAMEレコードを設定
3. 詳細は[GitHub Pages公式ドキュメント](https://docs.github.com/ja/pages/configuring-a-custom-domain-for-your-github-pages-site)を参照

## 他の公開方法

### Netlify Drop

1. [Netlify Drop](https://app.netlify.com/drop)にアクセス
2. `growing-photos.html` を `index.html` にリネーム
3. ファイルをドラッグ＆ドロップ
4. 即座に公開URL取得！

### Vercel

1. [Vercel](https://vercel.com)にログイン
2. 「New Project」をクリック
3. GitHubリポジトリをインポート
4. 自動的にデプロイ完了

どの方法も無料で利用できます！
