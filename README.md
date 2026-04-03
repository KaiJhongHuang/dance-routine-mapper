# Dance Routine Mapper

排舞圖表產生器 — 輸入動作序列，自動產生色彩對照表格。

## 功能

- 輸入每個動作的拍數與名稱，即時產生 8 拍為一列的色彩表格
- 用 `---` 分隔不同 Phase，支援多段落舞步
- 同色代表同一個動作，箭頭 `↓` 表示動作跨越 8 拍邊界延續
- 一鍵複製產生的 HTML，方便貼到筆記或網頁中

## 使用方式

### 線上使用

開啟 GitHub Pages：`https://kaijhonghuang.github.io/dance-routine-mapper/`

### 本地使用

直接用瀏覽器開啟 `generator.html` 即可，不需要任何伺服器或安裝。

## 輸入格式

每行一個動作，格式為 `拍數` + `動作名稱`：

```
6原地基本步
6Sendout
6Change Place
6Call Back
8Mini Dip
```

用 `---` 分隔不同 Phase：

```
6原地基本步
6Sendout
---
8Solo Turn
6Side Pass
```
