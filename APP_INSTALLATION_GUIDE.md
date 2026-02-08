# 🀄 麻雀スコア計算機 - アプリ化ガイド

## 📱 PWAとしてインストール（推奨・最も簡単）

このアプリはPWA（Progressive Web App）対応なので、ネイティブアプリのようにホーム画面に追加できます。

### iPhone/iPadでのインストール方法

1. Safariでアプリを開く
2. 画面下部の「共有」ボタン（□に↑マーク）をタップ
3. 「ホーム画面に追加」を選択
4. 「追加」をタップ
5. ホーム画面にアイコンが追加されます

### Androidでのインストール方法

1. Chromeでアプリを開く
2. 画面右上の「︙」メニューをタップ
3. 「ホーム画面に追加」または「アプリをインストール」を選択
4. 「インストール」をタップ
5. ホーム画面とアプリドロワーにアイコンが追加されます

### PWAの利点

✅ ストア審査不要で即座に使える
✅ インストールサイズが小さい（数KB）
✅ 自動更新
✅ オフラインでも動作
✅ ネイティブアプリのような操作感
✅ LocalStorageでデータ保存

---

## 🚀 ネイティブアプリ化（フル機能版）

### 方法1: Capacitor（推奨）

Capacitorを使えば、同じコードでiOSとAndroidアプリを作成できます。

```bash
# 必要なツールのインストール
npm install -g @capacitor/cli

# プロジェクト初期化
npx cap init "麻雀スコア計算機" "com.yourname.mahjong" --web-dir=.

# iOS追加
npx cap add ios
npx cap open ios  # Xcodeで開く

# Android追加
npx cap add android
npx cap open android  # Android Studioで開く
```

### 方法2: Cordova

```bash
# Cordovaインストール
npm install -g cordova

# プロジェクト作成
cordova create MahjongApp com.yourname.mahjong "麻雀スコア計算機"
cd MahjongApp

# ファイルをwww/にコピー
# mahjong-calculator.html → www/index.html

# プラットフォーム追加
cordova platform add ios
cordova platform add android

# ビルド
cordova build ios
cordova build android
```

### 方法3: React Native / Flutter（完全書き直し）

このHTMLアプリをReact NativeやFlutterで書き直す方法もありますが、時間がかかります。

---

## 📦 必要なファイル

アプリ化に必要なファイル：
- ✅ `mahjong-calculator.html` - メインアプリ
- ✅ `manifest.json` - PWA設定
- ✅ `service-worker.js` - オフライン対応
- ⚠️ `icon-192.png` - アプリアイコン（192x192）
- ⚠️ `icon-512.png` - アプリアイコン（512x512）

---

## 🎨 アイコン作成

アイコン画像が必要です。以下のサイズを用意：

- 192x192 px
- 512x512 px

推奨デザイン：
- 背景色：#667eea（紫のグラデーション）
- 中央に🀄絵文字または麻雀牌のイラスト
- シンプルで視認性の高いデザイン

オンラインツール：
- https://www.favicon-generator.org/
- https://realfavicongenerator.net/

---

## 🌐 ホスティング

アプリを公開するには、Webサーバーが必要です：

### 無料ホスティング
- **Vercel**: https://vercel.com （推奨）
- **Netlify**: https://netlify.com
- **GitHub Pages**: https://pages.github.com
- **Firebase Hosting**: https://firebase.google.com

### Vercelでのデプロイ（最も簡単）

1. GitHubアカウント作成
2. リポジトリ作成してファイルをプッシュ
3. Vercelでリポジトリを接続
4. 自動デプロイ完了！

```bash
# Vercel CLIを使う場合
npm i -g vercel
vercel --prod
```

---

## 📱 アプリストア公開（オプション）

### App Store（iOS）

必要なもの：
- Apple Developer Program（年間12,980円）
- Mac + Xcode
- Capacitor/Cordovaでビルド
- App Store Connect登録

### Google Play（Android）

必要なもの：
- Google Play Developer登録（初回$25）
- Capacitor/Cordovaでビルド
- APK/AABファイル作成

---

## 💡 推奨アプローチ

**個人利用・小規模配布** → PWAで十分！
- ホスティングして、URLをQRコードで共有
- インストール手順を伝えるだけ

**広く配布したい** → Capacitor + ストア公開
- より本格的なアプリとして配布
- プッシュ通知などの追加機能も可能

---

## 🔧 技術サポート

質問があれば、以下の情報を確認：
- PWA: https://web.dev/progressive-web-apps/
- Capacitor: https://capacitorjs.com/
- Cordova: https://cordova.apache.org/

---

開発者: Claude
バージョン: 1.0.0
ライセンス: MIT
