# 🎯 超簡単！Firebase設定ガイド（3ステップ）

## 📍 ステップ1: HTMLファイルで編集場所を見つける

### 方法1: 検索する（一番簡単！）

1. **mahjong-calculator.html** をメモ帳やテキストエディタで開く

2. **Ctrl + F** （Macは Cmd + F）で検索窓を開く

3. 以下を検索:
```
🔥 Firebase設定
```

4. すぐに見つかります！👇

---

## 📍 ステップ2: 見つかった場所

こんな感じの部分が見つかります：

```javascript
// ============================================================
// 🔥 Firebase設定 - ここを編集してください！
// ============================================================

const firebaseConfig = {
    apiKey: "YOUR_API_KEY",                    ← ここを置き換え
    authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
    // ... 以下省略
};
```

**この7行を編集します！**

---

## 📍 ステップ3: Firebaseの設定をコピーして貼り付け

### A. Firebaseコンソールを開く

1. https://console.firebase.google.com を開く
2. 作成したプロジェクトをクリック
3. 左上の **⚙️歯車アイコン** → **プロジェクトの設定**
4. 下にスクロール → **マイアプリ** セクション
5. **</>** （ウェブアプリ）をクリック

### B. 設定をコピー

画面にこのようなコードが表示されます：

```javascript
const firebaseConfig = {
  apiKey: "AIzaSyABC123...",           ← これをコピー
  authDomain: "my-app.firebaseapp.com", ← これをコピー
  databaseURL: "https://my-app-default-rtdb.firebaseio.com", ← これをコピー
  projectId: "my-app",                 ← これをコピー
  storageBucket: "my-app.appspot.com", ← これをコピー
  messagingSenderId: "123456789",      ← これをコピー
  appId: "1:123456789:web:abc123"      ← これをコピー
};
```

### C. HTMLファイルに貼り付け

**置き換え前:**
```javascript
const firebaseConfig = {
    apiKey: "YOUR_API_KEY",                    ← 消す
    authDomain: "YOUR_PROJECT_ID.firebaseapp.com", ← 消す
    databaseURL: "https://YOUR_PROJECT_ID-default-rtdb.firebaseio.com", ← 消す
    projectId: "YOUR_PROJECT_ID",              ← 消す
    storageBucket: "YOUR_PROJECT_ID.appspot.com", ← 消す
    messagingSenderId: "YOUR_MESSAGING_SENDER_ID", ← 消す
    appId: "YOUR_APP_ID"                       ← 消す
};
```

**↓ 置き換え後:**
```javascript
const firebaseConfig = {
    apiKey: "AIzaSyABC123...",                 ← 貼り付けた
    authDomain: "my-app.firebaseapp.com",      ← 貼り付けた
    databaseURL: "https://my-app-default-rtdb.firebaseio.com", ← 貼り付けた
    projectId: "my-app",                       ← 貼り付けた
    storageBucket: "my-app.appspot.com",       ← 貼り付けた
    messagingSenderId: "123456789",            ← 貼り付けた
    appId: "1:123456789:web:abc123"            ← 貼り付けた
};
```

---

## ✅ 確認方法

### 成功したか確認:

1. ファイルを保存
2. ブラウザでHTMLを開く
3. **F12キー**を押す（開発者ツール）
4. **Console**タブを見る
5. こう表示されればOK！✅
   ```
   Firebase initialized successfully
   ```

### まだ設定が必要な場合:
```
Firebase not configured. Using local mode only.
```
→ まだ「YOUR_API_KEY」のままになっています

---

## 🆘 よくある間違い

### ❌ 間違い1: 全部コピーしちゃった
```javascript
// これは間違い！
const firebaseConfig = {
const firebaseConfig = {  ← 2回になってる！
  apiKey: "...",
```

**正解:** `const firebaseConfig = {` は1回だけ！

---

### ❌ 間違い2: カンマを消しちゃった
```javascript
apiKey: "..."              ← カンマがない！
authDomain: "..."
```

**正解:** 最後の行以外は全部カンマ `,` が必要！

---

### ❌ 間違い3: ダブルクォートが消えた
```javascript
apiKey: AIzaSy...  ← " がない！
```

**正解:** 必ず `"` で囲む！

---

## 🎉 完了！

これで設定完了です！
「新しいゲーム作成」ボタンを押してテストしてみてください。

ルームコードが表示されれば成功です！🎊
