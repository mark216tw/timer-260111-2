# System Prompt: Bauhaus Timer (Compact)
    
## 🎯 專案目標
建立一個單檔案 (HTML/CSS/JS) 的包浩斯風格倒數計時器，強調「幾何構成」、「原色對比」與「無捲動緊湊佈局」。

## 🎨 視覺規範 (Bauhaus Style)
- **設計哲學**：Form Follows Function (形隨機能)，粗框線、硬陰影、幾何圖形。
- **色彩系統**：
  - **三原色**：紅 (#D02020)、藍 (#1040C0)、黃 (#F0C020)。
  - **基底**：極致黑 (#121212) 與 白 (#FFFFFF) 的高對比搭配。
- **字體**：'Outfit' (幾何無襯線體，Font Weight: 700/900)。
- **版面**：
  - **高度鎖定**：`height: 100vh; overflow: hidden;`，確保一屏顯示，無需捲動。
  - **卡片**：實心背景 + 粗黑框 (2px-4px) + 硬陰影 (無模糊)。
  - **進度環**：純幾何線條，方形端點 (stroke-linecap: square)。
- **主題**：
  - **Day**：米白底 + 黑框 + 原色點綴 (紅/藍/黃)。
  - **Night**：黑底 + 白框 + 原色點綴 (紅/藍/黃 pop out)。

## ⚙️ 核心功能
1. **時間調整**：幾何方塊按鈕 +/- 控制；原色色塊預設按鈕 (5/10/15/25/30)。
2. **音效系統**：Web Audio API (不依賴外部檔案)。
3. **快捷鍵**：Space (Start/Pause), R (Reset), Arrows (Adjust)。
4. **狀態保存**：LocalStorage (Theme, Title, Time)。

## 🔗 URL 狀態共享
- **參數**：`t` (初始秒), `s` (狀態), `start` (時間戳), `title` (標題)。
- **邏輯**：基於 Unix Timestamp 計算剩餘時間，確保跨裝置同步無誤差。

## 🛠 技術規格
- **Stack**：Native HTML5, CSS3, Vanilla JS (No Frameworks)。
- **Constraint**：Single File, Zero external assets (except Fonts).
