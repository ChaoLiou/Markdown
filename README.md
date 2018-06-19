- 目錄
  - [簡介](#簡介)
  - [標題](#標題)
      - [標題使用方式](#標題使用方式)
      - [其他方式](#其他方式)
  - [清單](#清單)
  - [常用字體](#常用字體)
  - [連結](#連結)
      - [連結使用方式](#連結使用方式)
      - [參考方式](#參考方式)
  - [表格](#表格)
  - [其他效果](#其他效果)
      - [引言](#引言)
      - [分隔線](#分隔線)
      - [工作清單](#工作清單)
      - [程式碼區塊](#程式碼區塊)
      - [使用emoji](#使用emoji)

## 簡介
### `Markdown` 是一種 `輕量級` `標記式` 語法 (lightweight markup language)
- `輕量級`: 意思是指 規則**少**, 而且都很**簡單**
- `標記式`: 意思是指 只要根據 `Markdown` 的規則, 在文章中標記一些 `符號`, 在呈現網頁畫面時, 即可產生你預期的效果

> 看到這邊, 應該有發現, 文章到目前為止, 已經有使用一些效果了, 以下開始介紹 `標記甚麼符號` -> `會達到甚麼效果`

參考自 [Github Markdown](https://help.github.com/articles/basic-writing-and-formatting-syntax/)

---

### 標題
#### 標題使用方式
- 標記 `#` 會呈現 `標題` 的效果, `#` 越 **多**, `標題` 字體越小越細

寫法:

```markdown
# H1
## H2
### H3
#### H4
##### H5
###### H6
```

呈現:

# H1
## H2
### H3
#### H4
##### H5
###### H6

---
#### 其他方式
- 在 `標題` 文字下方標記 `=` 與 `-`(可以只標記一個), 呈現等同於 `# ` 與 `## `效果

寫法:

```markdown
H1
=

H2
-
```

呈現:

H1
=

H2
-

---
### 清單
- `清單` 分為 `無序`(Unordered) 與 `有序`(Ordered), **序**指的是**順序**, `無序` 也等同於 `子彈式` (Bulleted)

寫法:

```markdown
// 無序
- 1st item
- 2nd item
- 3rd item

// 有序
1. item
2. item
3. item
```

呈現:

- 1st item
- 2nd item
- 3rd item

1. item
2. item
3. item

---
### 常用字體
- 粗體 (bold)
- 斜體 (italic)
- 刪除線 (strikethrough)

寫法:

```markdown
// 粗體
**bold**
__bold__

// 斜體
*italic*
_italic_

// 組合使用
__bold *italic*__
**bold _italic_**

// 刪除線
~~strikethrough~~
```

呈現:

**bold**

__bold__

*italic*

_italic_

__bold *italic*__

**bold _italic_**

~~strikethrough~~

---
### 連結
#### 連結使用方式
寫法:

```markdown
[google](https://www.google.com)
[google, 游標移上來會有提示文字](https://www.google.com 'a link to google')
[使用相對於目前網址的路徑](./)
```

[google](https://www.google.com)

[google, 游標移上來會有提示](https://www.google.com 'a link to google')

[使用相對於目前網址的路徑](./)

---
#### 參考方式
- 在整份文件中, 當有 **連結很常用到**, 可以使用 `參考`

```markdown
[google link]
[這會連到 google][google link]
[這會連到 google 但是參考名稱是1][1]

// 定義參考
[google link]: https://www.google.com
[1]: https://www.google.com
```

[google link]

[這會連到 google][google link]

[這會連到 google][1]

[google link]: https://www.google.com
[1]: https://www.google.com

---
#### 圖片
- 與 `連結` 用法很相近, 唯二不一樣的地方是 1. `圖片` 要在最前面加上 `!`, 2. \[文字\](網址): `連結` 的 `文字` 是網址顯示的文字, 圖片的 `文字` 是 img 的 alter attribute (alter = alternative, 當圖片網址下載失敗, 會顯示 alter attribute)

寫法:

```markdown
![google](http://icons.iconarchive.com/icons/danleech/simple/256/google-icon.png)
![image not found](http://xxx/abc.png)
```

呈現:

![google](http://icons.iconarchive.com/icons/danleech/simple/256/google-icon.png)

![image not found](http://xxx/abc.png)

---
### 表格
- 只要掌握 2 個原則 
  1. 第一行 `|` 的數量 = 第二行 `|` 的數量
  2. 第二行每個格子裡的 `-` 至少要3個
- 還能設定 Column 靠左, 靠右或置中

寫法:

```markdown
|Table|1st Column(Left)|2nd Column(Middle)|3rd Column(Right)|
|---|:---|:---:|---:|
|1st Row|Hi|Hi|Hi|
|2nd Row|Hi|Hi|Hi|
|3rd Row|Hi|Hi|Hi|
```

|Table|1st Column(Left)|2nd Column(Middle)|3rd Column(Right)|
|---|:---|:---:|---:|
|1st Row|Hi|Hi|Hi|
|2nd Row|Hi|Hi|Hi|
|3rd Row|Hi|Hi|Hi|

---
### 其他效果
#### 引言

寫法:
```markdown
> E = mc^2
>           - Albert Einstein
```

呈現:

> E = mc^2
>           - Albert Einstein

---
#### 分隔線
- 可以使用 `-`, `*`, `_` 3種符號標記, 至少3個

寫法:

```markdown
---
```

呈現:

開始

---

結束

---
#### 工作清單
- 組合 `清單` + `核取方塊(checkbox)` 的效果, 會在清單項目起始加上 `核取方塊(checkbox)`, 常用來表示清單上的工作項目完成或未完成
- 注意只能配合 `-` 使用

寫法:

```markdown 
- [x] 寫 Markdown 文件
- [ ] 寫 Git 文件
- [ ] 推廣大家使用
```

呈現:

- [x] 寫 Markdown 文件
- [ ] 寫 Git 文件
- [ ] 推廣大家使用

---
#### 程式碼區塊
- 以選擇的程式語言呈現程式碼, 支援許多程式語言

呈現:

```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```

```python
s = "Python syntax highlighting"
print s
```

```
沒有指定程式語言, 所以不會把關鍵字上色
```

---
#### 使用emoji
- 標記 emoji 代碼, 網頁就會呈現 emoji

:bowtie:
:smile:
:laughing:
...

其他 emoji 參考 [Emoji Cheat Sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet/)
