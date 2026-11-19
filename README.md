# 小豬存錢筒 PWA 外殼

這個網頁只負責「手機桌面圖示」，點開後會跳到 GAS 記帳本，記帳資料仍存在 Google 試算表。

## 設定
打開 `index.html`，把這一行換成你的 GAS 網頁應用程式網址（結尾 `/exec`）：

```js
const GAS_URL = 'https://script.google.com/macros/s/請貼上你的部署ID/exec';
```

## 部署到 GitHub Pages
1. GitHub 新增 repository（例如 `piggy-bank`，設為 Public）。
2. 上傳本資料夾全部檔案（含 `icons/` 資料夾）。
3. Settings → Pages → Source 選 `Deploy from a branch`，Branch 選 `main` / `(root)` → Save。
4. 約 1 分鐘後網址為 `https://你的帳號.github.io/piggy-bank/`。

## 加入手機桌面
- iPhone：Safari 開啟網址 → 分享 → 加入主畫面
- Android：Chrome 開啟網址 → ⋮ → 安裝應用程式／加到主畫面

## 注意
- 更換圖示後，手機要先刪除舊的桌面圖示再重新加入才會更新。
- 修改檔案後如果手機沒更新，把 `sw.js` 裡的 `piggy-shell-v1` 改成 `v2`。
