# Release Notes

## v1.1 (2026-04-03)

新增子步法記譜功能，可在動作內標記每段拍的步法細節。

### 新功能

- **子步法記譜語法**：在動作下方用縮排行標記步法細節
  ```
  6 Send Out
    2 Rock Step
    2 Triple Step
    2 Triple Step
  ```
- **「顯示細節」切換按鈕**：位於圖表上方，一鍵切換總覽與細節模式
- **圖表細節模式**：展開為雙列顯示
  - 上方：主動作名稱，完整跨格顯示
  - 下方：子步法名稱，拆分為獨立小格，較小字體（10px）、較淺底色
- **動作順序區**：細節模式下同步顯示子步法列表
- **預設範例更新**：default 預設加入子步法示範
  - 第一段（6 拍動作）：Rock Step → Triple Step → Triple Step
  - 第二段（8 拍動作）：Rock Step → Triple Step → Step Step → Triple Step

### 設計原則

- 向下相容：沒有子步法的動作行為與 v1.0 完全相同
- 子步法為可選功能，不影響既有記譜格式
- 格式說明區已更新，提示縮排子步法語法

---

## v1.0 (2026-04-03)

首次正式版本發布。

### 核心功能
- 輸入動作拍數與名稱，即時產生 8 拍為一列的色彩對照表格
- 同色代表同一個動作，`↓` 箭頭標示動作跨越 8 拍邊界延續
- 支援多段落分隔（`T 段落名稱` 或 `---`）
- 8 拍列自動編號，跨段落連續計數
- 動作順序摘要區塊，快速確認舞序

### 內建經典排舞預設
- Shim Sham（4 段：Stomp Off、Cross Over、Tack Annie、Half Break）
- Big Apple（2 段，動作順序依據 Frankie Manning 編舞的 Keep Punching 1939 版本校正）

### 技術
- 純前端靜態網頁，無需後端
- GitHub Pages 部署
- URL 參數載入預設排舞（`?routine=shim-sham`、`?routine=big-apple`）
