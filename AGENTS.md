# 三國志戰略版 - 攻略百科 AI 開發指南

## 1. 專案目的 (Project Purpose)
這是一個基於《(20261103)秋石小軍師三戰漢焰長明劇本攻略.pdf》的靜態知識庫網站。
目標是讓 AI 能根據我提供的隊伍名稱（如：皇馬槍、五謀騎），自動輸出結構一致、帶有完整戰法表格的陣容攻略網頁。

## 2. 檔案結構 (File Structure)
- `index.html`：攻略總目錄。
- `css/style.css`：全站共用的樣式表。
- `lineups/`：存放所有具體陣容攻略的資料夾（例如 `lineups/huang-ma-qiang.html`）。

## 3. 頁面結構與新增規則 (Page Structure & Rules)
當我要求你「新增一篇三戰陣容攻略」時，你必須遵守以下 HTML 結構與開發規則：

1. **檔案命名**：必須全小寫，使用連字號分隔的英文拼音，副檔名為 `.html`。
2. **HTML 骨架**：
   - 必須引入 `../css/style.css`。
   - `<header>` 內需包含 `<a href="../index.html" class="back-btn">← 返回首頁</a>`，以及陣容名稱 `<h1>`。
3. **內容區塊 (Content Blocks)**：
   頁面 `<main>` 中必須包含以下三個區塊：
   - `<section class="team-info">`：標註該陣容的「強度評級（如 T0, T1）」與「所屬陣營（如 蜀、魏、群）」。
   - `<section class="lineup-table">`：**必須使用 HTML `<table>`** 呈現武將搭配。表格需包含 6 個欄位：`武將`、`加點`、`第二戰法`、`第三戰法`、`兵書`、`裝備`。主將必須放在表格第一列。
   - `<section class="strategy-notes">`：包含「奇謀武略」的選擇建議，以及「注意事項/說明」的段落。

## 4. AI 協作指令範例
當我輸入：「請依照 AGENTS.md 新增一篇『T0 五謀騎 (SP荀彧、SP郭嘉、賈詡)』的攻略」，請直接輸出完整的 HTML 程式碼，確保表格標籤與 CSS class 完全符合上述規定。