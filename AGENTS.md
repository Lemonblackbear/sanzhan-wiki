# 三戰漢焰長明攻略百科 AI 開發指南

## 1. 專案目的
將《(20261103)秋石小軍師三戰漢焰長明劇本攻略.pdf》轉化為靜態知識庫。
目標是讓 AI 能夠根據指示，自動判斷文章類型，並套用對應的版型與資料夾結構。

## 2. 資料夾結構與命名規則
AI 必須根據我要求的「文章類型」來決定檔案位置：
- **陣容配將 (Lineups)**：放在 `lineups/` 資料夾。
- **機制教學 (Guides)**：放在 `guides/` 資料夾（如：開荒技巧、碰瓷教學）。
- **檔案命名**：全小寫、連字號分隔 (Kebab-case)，副檔名為 `.html`。

## 3. 頁面模板與固定段落
所有新建頁面 `<main>` 內必須包含以下結構，並確保引入 `../css/style.css`。

### 類型 A：陣容配將 (Lineups)
1. **陣容評級**：`<section class="team-info">` 標註強度與陣營。
2. **配將表格**：`<section class="lineup-table">` 必須使用 `<table>`，強制 6 個欄位：`武將`, `加點`, `第二戰法`, `第三戰法`, `兵書`, `裝備`。主將放第一列。
3. **攻略說明**：`<section class="strategy-notes">` 包含奇謀武略與注意事項。

### 類型 B：機制教學 (Guides)
1. **教學前言**：`<section class="guide-intro">` 用 2-3 句話總結這篇教學的核心目的。
2. **核心觀念**：`<section class="guide-content">` 使用 `<h3>` 標題與條列式 `<ul>` 整理核心機制。
3. **實戰建議**：`<section class="strategy-notes">` 補充實戰中的避坑指南。

## 4. 完成檢查清單 (AI Checklist)
- [ ] 檔案是否放在正確的資料夾 (`lineups/` 或 `guides/`)？
- [ ] 樣式表路徑 `../css/style.css` 是否正確？
- [ ] 若為陣容頁面，表格 `<table>` 是否具備 6 個欄位？
