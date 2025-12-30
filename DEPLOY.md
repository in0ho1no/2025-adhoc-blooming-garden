# GitHub Pagesへの公開手順

## 手順

### 1. GitHubリポジトリの作成

1. [GitHub](https://github.com)にログイン
2. 右上の「+」から「New repository」をクリック
3. リポジトリ名を入力（例：`blooming-garden`）
4. 「Public」を選択
5. 「Create repository」をクリック

### 2. ファイルのアップロード

#### 方法A: ブラウザから直接アップロード（推奨・簡単）

1. 作成したリポジトリのページで「uploading an existing file」をクリック
2. `index.html` をそのままアップロード
3. 「Commit changes」をクリック

#### 方法B: Git コマンドを使用

```bash
# リポジトリをクローン
git clone https://github.com/YOUR_USERNAME/blooming-garden.git
cd blooming-garden

# ファイルをコピー
cp /path/to/index.html index.html

# コミット＆プッシュ
git add index.html
git commit -m "Add Blooming Garden game"
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
https://YOUR_USERNAME.github.io/リポジトリ名/
```

例：`https://in0ho1no.github.io/2025-adhoc-blooming-garden/`

## 注意事項

- ファイル名は `index.html` のままでOKです
- GitHub Pagesは無料で利用できます
- 変更を加えた場合は、同じ手順でファイルを更新するだけでOKです
- HTTPSで自動的に配信されます

## カスタムドメインの設定（オプション）

独自ドメインを使いたい場合：

1. GitHub Pages設定で「Custom domain」にドメインを入力
2. DNSプロバイダーでCNAMEレコードを設定
3. 詳細は[GitHub Pages公式ドキュメント](https://docs.github.com/ja/pages/configuring-a-custom-domain-for-your-github-pages-site)を参照
