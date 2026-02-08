# 🚀 簡単デプロイガイド

## 最も簡単な方法：Vercel

### 手順

1. **GitHubアカウント作成**
   - https://github.com にアクセス
   - Sign upから登録

2. **新しいリポジトリ作成**
   - 「New repository」をクリック
   - 名前: `mahjong-calculator`
   - Publicを選択
   - Create repository

3. **ファイルをアップロード**
   - 「uploading an existing file」をクリック
   - 以下のファイルをドラッグ＆ドロップ：
     - mahjong-calculator.html
     - manifest.json
     - service-worker.js
     - icon-192.png（作成した場合）
     - icon-512.png（作成した場合）
   - Commit changes

4. **Vercelでデプロイ**
   - https://vercel.com にアクセス
   - 「Sign Up」→「Continue with GitHub」
   - リポジトリを選択してImport
   - Deploy をクリック
   - 完了！URLが発行されます

5. **スマホで開く**
   - 発行されたURLをスマホで開く
   - ホーム画面に追加
   - アプリとして使用開始！

---

## アイコンの作成

アイコンがない場合、以下のサイトで無料作成：

1. https://www.canva.com にアクセス
2. カスタムサイズ：512 x 512 px
3. 背景色を紫系（#667eea）に
4. 中央に🀄絵文字を配置
5. PNG形式でダウンロード
6. オンラインツールで192pxにリサイズ

または、絵文字をそのまま使うこともできます。

---

## トラブルシューティング

**Q: PWAとしてインストールできない**
A: HTTPSが必要です。Vercelなら自動でHTTPS化されます。

**Q: オフラインで動かない**
A: Service Workerの登録を確認。開発者ツールのApplicationタブで確認できます。

**Q: データが消える**
A: LocalStorageを使用しているため、ブラウザキャッシュをクリアすると消えます。

---

所要時間：約10分
費用：無料
