# HTML5 語意化標籤

頁面標籤範例
![主體](https://hackmd.io/_uploads/S1vxv55Mee.png)

main article 標籤範例
![article](https://hackmd.io/_uploads/SJi6w55Mgl.png)

main section 標籤範例
![section](https://hackmd.io/_uploads/Hy0nuqqzex.png)

## 1. 頁首標籤 `<header>`
`<header>` 標籤如果是在 `<body>` 內，它可以表示網頁的頁首，但如果位於 `<article>` 或 `<section>` 內，則可以表示文章或區塊內的首要區塊。

### 放在 `<body>` 內範例
```html
<header>
  <div class="banner">
    <div class="banner-photo"></div>
    <div class="banner-content">
      <h2>標題</h2>
      <p>內容</p>
    </div>
  </div>
</header>
```
![image](https://hackmd.io/_uploads/HyF6itqMge.png)

---

## 2. 導覽列 `<nav>`
只要是在網站內的導覽區塊，都適合使用 `<nav>` 標籤（navigation 導航之意），像是主選單、頁尾選單等。
```html
<nav>
  <ul>
    <li><a href="#">功能一</a></li>
    <li><a href="#">功能二</a></li>
    <li><a href="#">功能三</a></li>
  </ul>
</nav>
```
![image](https://hackmd.io/_uploads/SJtD2K9zxx.png)

---

## 3. 主要區塊 `<main>`
用來放置網頁主要資訊的區塊，展現網頁內容的獨特性。每個頁面只能有一個 `<main>` 標籤，且理想狀態下，不能被放在 `<nav>`、`<article>`、`<aside>`、`<footer>` 和 `<header>` 內。

---

## 4. 區塊或文章區塊 `<article>` `<section>`
- `<section>`：搭配 `<h1~h6>` 的標題來呈現區塊內容。
- `<article>`：主要用於包覆完整的「文章」內容。
- `<div>`：這時可以視作一個「無意義」的容器，僅為了排版目的使用。

---

## 5. 側欄 `<aside>`
`<aside>` 語意算是跟主要區塊內容無關的區塊，也就是額外資訊，像是側邊欄、廣告、推薦文章等。

---

## 6. 頁尾 `<footer>`
表示頁首或表尾部分，使用方式同 `<header>`。

---

## 7. 其他常用語意標籤
- **時間 `<time>`**：用來表示日期時間，加上 `datetime="YYYY-MM-DD"` 讓搜尋引擎能解析。
- **註記 `<mark>`**：像螢光筆一樣註記重點。
- **圖表包覆 `<figure>`**：包覆圖像、插圖或程式碼，可搭配 `<figcaption>` 提供說明。

### 範例：使用 `<figure>` 包覆圖片
```html
<figure>
  <img src="performance.jpg" alt="網頁效能優化示意圖">
  <figcaption>瀏覽器快取可提升載入速度</figcaption>
</figure>
```
![image](https://hackmd.io/_uploads/S1SBbq9zeg.png)
