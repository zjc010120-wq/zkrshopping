# 代購報價計算器 App

可安裝的網頁 App（PWA）：手機、平板、電腦都能開，可加到主畫面、全螢幕開啟、離線使用。

## 檔案

| 檔案 | 用途 |
|---|---|
| `index.html` | App 本體（計算／紀錄／設定三個頁面） |
| `manifest.webmanifest` | App 名稱、圖示、顏色，讓手機和電腦可以「安裝」 |
| `sw.js` | 離線快取與自動更新 |
| `icons/` | App 圖示 |

## 上線（GitHub Pages，免費）

1. 到 github.com 建立帳號，按右上角 **+ → New repository**，名稱例如 `daigou`，選 **Public**，建立。
2. 在新的 repository 頁面按 **uploading an existing file**，把這個 `app` 資料夾裡的**所有檔案與 `icons` 資料夾**拖進去，按 **Commit changes**。
3. 進 **Settings → Pages**，Source 選 **Deploy from a branch**，Branch 選 `main` / `(root)`，按 **Save**。
4. 約 1 分鐘後網址會出現在同一頁，例如 `https://你的帳號.github.io/daigou/`。

用手機打開這個網址，就能依「設定 → 安裝成 App」的說明加到主畫面。

## 之後要更新

1. 修改檔案後，把 `sw.js` 第 3 行的 `VERSION` 改成新號碼（例如 `v1.0.1`），`index.html` 裡的 `VERSION` 也一起改。
2. 重新上傳到 GitHub。
3. 使用者下次開 App 時會看到「有新版本可用 · 重新整理」。

## 注意

- 資料（紀錄、常用設定）存在各自裝置的瀏覽器裡，不會在手機和電腦之間同步。要搬資料請用「設定 → 下載備份／還原備份」。
- 必須用 `https://` 網址開啟才能安裝與離線使用（GitHub Pages、Netlify、Cloudflare Pages 都符合）。
