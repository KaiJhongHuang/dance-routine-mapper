# 用 Claude 產生排舞圖表

你可以請 Claude 幫你把任何排舞整理成標準格式，再貼到 [Dance Routine Mapper](https://kaijhonghuang.github.io/dance-routine-mapper/generator.html) 產生圖表。

---

## 記譜格式規則

```
舞序名稱
T 段落名稱
拍數 動作名稱
拍數 動作名稱
  拍數 子步法名稱
  拍數 子步法名稱

T 第二段名稱
拍數 動作名稱
```

### 規則

| 項目 | 格式 | 說明 |
|------|------|------|
| 舞序名稱 | 第一行，純文字 | 不能是 `T` 開頭，也不能是 `數字 文字` 格式 |
| 段落標題 | `T 段落名稱` | 用 `T` 加空格開頭 |
| 動作 | `拍數 動作名稱` | 如 `6 Send Out`、`8 Swing Out` |
| 子步法 | `  拍數 子步法名稱` | **必須縮排**（2 個空格開頭），歸屬上一個動作 |
| 空行 | 空行 | 段落之間留空行增加可讀性（可選） |

### 注意事項

- 拍數必須是數字，且與動作名稱之間有空格
- 子步法的拍數加總應等於主動作的拍數
- 常見的 Swing Dance 子步法組合：
  - 6 拍動作：`2 Rock Step` → `2 Triple Step` → `2 Triple Step`
  - 8 拍動作：`2 Rock Step` → `2 Triple Step` → `2 Step Step` → `2 Triple Step`

---

## 完整範例

```
Shim Sham
T Stomp Off
8 Stomp Off (R)
8 Stomp Off (L)
8 Stomp Off (R)
8 Break

T Cross Over
8 Cross Over (R)
8 Cross Over (L)
8 Cross Over (R)
8 Break

T Tack Annie
8 Tack Annie
8 Tack Annie
8 Tack Annie
8 Break

T Half Break
8 Half Break
8 Half Break
8 Half Break
8 Break
```

### 含子步法的範例

```
Lindy Hop 基本組合
T 第一段
6 Send Out
  2 Rock Step
  2 Triple Step
  2 Triple Step
6 Change Place
  2 Rock Step
  2 Triple Step
  2 Triple Step
8 Break

T 第二段
8 Swing Out
  2 Rock Step
  2 Triple Step
  2 Step Step
  2 Triple Step
8 Lindy Circle
  2 Rock Step
  2 Triple Step
  2 Step Step
  2 Triple Step
```

---

## 如何使用

1. 請 Claude 幫你整理排舞（參考下方 Prompt 範例）
2. 複製 Claude 輸出的文字
3. 開啟 [Dance Routine Mapper](https://kaijhonghuang.github.io/dance-routine-mapper/generator.html)
4. 貼上文字到輸入區
5. 點「分享連結」取得可分享的 URL

---

## Prompt 範例

### 基本

> 請幫我整理這個排舞，用 Dance Routine Mapper 的格式輸出：
> Shim Sham 四段，每段三個重複動作加一個 Break...

### 指定子步法

> 請幫我把以下 Lindy Hop routine 整理成 Dance Routine Mapper 格式，每個動作加上子步法（Rock Step、Triple Step 等）：
> 第一段：Send Out, Change Place, Call Back, Break
> 第二段：Swing Out x2, Texas Tommy, Lindy Circle

### 從影片或口述

> 我在課堂上學了一個排舞，順序是：
> 8拍 Swing Out 做兩次，然後 Texas Tommy，最後 Lindy Circle
> 請用 Dance Routine Mapper 格式輸出，含子步法

---

## 給 Claude 的系統提示（可選）

如果你想讓 Claude 每次都自動輸出正確格式，可以在對話開頭加上：

> 當我請你整理排舞時，請用以下格式輸出：
> - 第一行是舞序名稱
> - 用 `T 段落名稱` 分段
> - 每行格式為 `拍數 動作名稱`
> - 子步法用兩個空格縮排
> - 輸出純文字，不要用 code block 包裹，方便我直接複製貼上
