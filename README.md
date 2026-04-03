# Dance Routine Mapper

排舞圖表產生器 — 輸入動作序列，自動產生色彩對照表格。

**線上使用：** https://kaijhonghuang.github.io/dance-routine-mapper/

## 功能

- 輸入每個動作的拍數與名稱，即時產生 8 拍為一列的色彩表格
- 用 `Phase N` 或 `---` 分隔不同 Phase，支援多段落舞步
- Phase 可加描述：`Phase 1 — Stomp Off`
- 同色代表同一個動作，箭頭 `↓` 表示動作跨越 8 拍邊界延續
- 內建經典排舞預設：Shim Sham、Big Apple

## 輸入格式

每行一個動作，格式為 `拍數` + `動作名稱`，用 `Phase N` 分隔段落：

```
Phase 1
6 6 Count Basic
6 Send Out
6 Change Place
6 Call Back
8 Break

Phase 2
8 Swing Out
8 Swing Out
8 Texas Tommy
8 Lindy Circle
```
