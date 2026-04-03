# Release Notes

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
