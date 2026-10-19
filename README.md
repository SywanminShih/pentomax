# PentoMAX Box Game：放上網路的方法

這個資料夾就是完整的網頁 App，不需要安裝、不需要伺服器程式。
上傳到任何「靜態網站」服務，就能用網址在電腦和手機上直接玩。

## 檔案
- `index.html`：遊戲本身（9 個 3D 題目、AI 檢查、提示、Live JSON）
- `manifest.webmanifest`、`icon-192.png`、`icon-512.png`：讓手機能「加入主畫面」，像 App 一樣全螢幕開啟
- `sw.js`：第一次開過以後，沒有網路也能玩

## 方法 A：Replit（和你現在的 pentomino-game 一樣）
1. Replit → Create App → 選 **HTML, CSS, JS** 範本。
2. 刪掉範本裡的檔案，把這個資料夾的所有檔案拖進去。
3. 按 **Run** 先試玩；沒問題後按 **Deploy** → **Static**，就會得到 `xxx.replit.app` 的網址。

## 方法 B：Netlify Drop（最快，約 1 分鐘）
1. 打開 https://app.netlify.com/drop
2. 把整個資料夾拖進頁面，馬上得到網址；登入後可以改成自己的名稱。

## 方法 C：GitHub Pages（免費、適合長期維護）
1. 在 GitHub 建一個新的 repository，上傳這些檔案。
2. Settings → Pages → Branch 選 `main`、資料夾選 `/ (root)` → Save。
3. 約 1 分鐘後網址是 `https://你的帳號.github.io/repository 名稱/`。

## 在手機上變成 App
- iPhone：用 Safari 打開網址 → 分享 → **加入主畫面**。
- Android：用 Chrome 打開網址 → 選單 → **安裝應用程式**／加入主畫面。

## 更新題目
題目資料在 `index.html` 裡的 `const PUZZLES=[...]`，格式和 `challenge_0xx_3d.json` 的 layers 相同。
