# Dance Routine Mapper

排舞圖表產生器 — 輸入動作序列，自動產生色彩對照表格。

**線上使用：** https://kaijhonghuang.github.io/dance-routine-mapper/

## 功能

- 輸入每個動作的拍數與名稱，即時產生 8 拍為一列的色彩表格
- 用 `T` 標記段落標題，支援多段落舞步
- 同色代表同一個動作，箭頭 `↓` 表示動作跨越 8 拍邊界延續
- 內建經典排舞預設：Shim Sham、Big Apple（動作順序依據 1939 年 Keep Punching 影片版本）
- **子步法記譜**：用縮排標記動作內的步法細節（如 Rock Step、Triple Step）
- **「顯示細節」切換**：一鍵切換總覽 / 細節檢視模式

## 輸入格式

每行一個動作，格式為 `拍數` + `動作名稱`，用 `T` + `標題` 分隔段落：

```
T Part 1
8 Swing Out
8 Texas Tommy
6 Send Out
6 Change Place

T Part 2
8 Lindy Circle
8 Charleston
8 Break
```

### 子步法（v1.1 新增）

在動作下方用縮排標記每段拍的步法細節：

```
6 Send Out
  2 Rock Step
  2 Triple Step
  2 Triple Step
8 Swing Out
  2 Rock Step
  2 Triple Step
  2 Step Step
  2 Triple Step
```

點擊「顯示細節」按鈕後，圖表會展開為雙列顯示：
- 上方：主動作名稱（完整跨格）
- 下方：子步法（拆分小格、較小字體、較淺底色）

沒有子步法的動作不受影響，完全向下相容。

## 版本紀錄

### v1.1

- 新增子步法記譜語法（縮排子行）
- 新增「顯示細節」切換按鈕
- 圖表細節模式：主動作在上、子步法在下，雙列顯示
- 動作順序區同步顯示子步法
- 預設範例加入子步法示範

### v1.0

- 圖表產生器：輸入動作序列，即時產生 8 拍色彩對照表格
- 支援多段落（`T` 標題分隔）與跨拍動作顯示（`↓` 箭頭）
- 內建經典排舞預設：Shim Sham（4 段）、Big Apple（2 段）
- Big Apple 動作順序已校正，依據 Frankie Manning 編舞的 Keep Punching (1939) 版本
