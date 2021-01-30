# CSSのコーディング②_細かなスタイルの指定

## ヘッダーとロゴ画像のスタイル指定

- ヘッダーを中央揃えに配置
  - `margin: 0 auto;`
- ロゴをヘッダー内の中央に配置
  - `text-align: center;`

```html
<header class="header">
  <h1 class="logo">
    <img src="../img/kamocafelogo-1.png" alt="kamocafe">
  </h1>
</header>
```

```css
.header {
  min-width: 8vw;
  max-width: 18vw;
  margin: 0 auto;
  padding: 20px 0;
}

.logo {
  margin: 0;
  text-align: center;
}
```

## メインコンテンツ全体とメインイメージのスタイル指定

```html
<main class="main">
  <figure class="top">
    <img src="../img/debby-hudson-FO4gzqI2t84-unsplash.jpg" alt="お茶と紙と花の写真">
  </figure>
︙
</main>
```

```css
.main {
  width: 95vw;
  max-width: 1000px;
  margin: 0 auto;
}

.top {
  margin-bottom: 20px;
  text-align: center;
}
```

## ナビゲーションのスタイル指定

`li` 要素を横並びにするため、 `display:inline-block;`  
項目の間に境界線（|　縦棒）を表現するため、 `border-left` を指定  
最初の `li` 要素には縦棒を表示させたくないため、 `:first-child { border-left: none; }` にしている

```html
<nav class="nav">
  <ul class="nav-list">
    <li><a href="#about">about</a></li>
    <li><a href="#menu">menu</a></li>
    <li><a href="#photos">photos</a></li>
    <li><a href="#access">access</a></li>
  </ul>
</nav>
```

```css
.nav {
  margin-bottom: 50px;
  text-align: center;
}

/* li指定 */
.nav-list li {
  display: inline-block;
  margin: 0;
  border-left: 1px solid #806342;
}
/* 疑似クラスを指定 */
.nav-list li:first-child {
  border-left: none;
}
/* aタグに指定 */
.nav-list a {
  display: inline-block;
  padding: 0 15px;
  line-height: 1.2;
  text-transform: uppercase;
}
```

## 4つのsectionのスタイル指定

共通で使う `section` と見出し画像の設定をする

```html
<section class="section about" id="about">
  <h2 class="heading">　〜　</h2>
  <p>　〜　</p>
</section>
︙
<section class="section menu" id="menu">
  <h2 class="heading">　〜　</h2>
  <ul>　〜　</ul>
</section>
︙
<section class="section photos" id="photos">
  <h2 class="heading">　〜　</h2>
  <ul>　〜　</ul>
</section>
︙
<section class="section access" id="access">
  <h2 class="heading">　〜　</h2>
  <div>　〜　</div>
</section>
```

```css
.section {
  margin: 0 auto 80px;
}

.heading {
  margin-bottom: 40px;
  text-align: center;
}
```

## 「about」セクションの指定

`section` の中の要素を中央揃えにする

```html
<section class="section about" id="about">
  <h2 class="heading">　〜　</h2>
  <p>　〜　</p>
</section>
```

```css
.about {
  text-align: center;
}
```

## 「menu」セクションの指定

`section` の中の要素を中央揃えにする  
`ul` を `section` に対して左右中央に配置する  
`li` は `ul` に対して左寄せにする

```html
<section class="section menu" id="menu">
  <h2 class="heading">
    <img src="../img/menu.svg" alt="menu">
  </h2>
  <ul class="menu-list">
    <li>カモミールティー ・・・ 300円</li>
    <li>ルイボスティー ・・・ 400円</li>
    <li>そば茶 ・・・ 300円</li>
    <li>黒豆茶 ・・・ 400円</li>
  </ul>
</section>
```

```css
.menu {
  text-align: center;
}
.menu-list {
  display: inline-block;
  margin-left: 30px;
  list-style: disc;
  text-align: left;
}
.menu-list li {
  margin-bottom: 10px;
}
```

## 「photos」セクションの指定

`section` 内の要素の横幅を全体に広げ内容に、指定する  
`li` 要素の下に `margin` を設ける

```html
<section class="section photos" id="photos">
  <h2 class="heading">
    <img src="../img/photos.svg" alt="photos">
  </h2>
  <ul class="photos-list">
    <li>
      <figure>
        <img src="../img/calm-place.jpg" alt="静かに過ごせるスペース">
        <figcaption>　〜　</figcaption>
      </figure>
    </li>
    <li>
      <figure>　〜　</figure>
    </li>
    <li>
      <figure>　〜　</figure>
    </li>
  </ul>
</section>
```

```css
.photos {
  width: 50vw;
  max-width: 750px;
}

.photos-list li {
  margin-bottom: 30px;
}

.photos figcaption {
  font-size: 12px;
  text-align: left;
}
```

## 「access」セクションの指定

`section` 内の要素の横幅を全体に広げ内容に、指定する  
`address` と `figure` を `div` で囲い、 `display:flex;` にすることで、横並びにする  
`address` に文字サイズ、 `display: block;` を指定する

```html
<section class="section access" id="access">
  <h2 class="heading">
    <img src="../img/access.svg" alt="access">
  </h2>
  <div class="access-row">
    <address class="access-address">
      <strong>
        Caffeine-Free Drinks Tea Shop
      </strong><br>
      〒 123-4567<br>
      東京都杉並区高円寺北 0-00<br>
      <strong>
        TEL 012-345-6789
      </strong>
    </address>
    <div class="access-map">
      <iframe>　〜　</iframe>
    </div>
  </div>
</section>
```

```css
.access {
  min-width: 40vw;
  max-width: 700px;
}

.access-row {
  /* flexbox指定　*/
  display: flex;
  justify-content: space-around;
  align-items: center;
  margin: 0 auto;
}

.access-address {
  /* address 指定 */
  font-size: 14px;
}

.access-address strong {
  display: block;
  margin: 10px 0;
  font-size: 22px;
}

.access-map {
  /* map 指定 */
  overflow: hidden;
  padding-bottom:20%;
  position: relative;
  height: 0;
  width: 30%;
}

.access-map iframe {
  left: 0;
  top: 0;
  height: 100%;
  width: 100%;
  position: absolute;
}
```

## フッターのスタイル指定

`footer` 内の要素を左右中央揃えにする  
ロゴ画像とナビゲーション/コピーライトを横並びにする  
ナビゲーション/コピーライトの文字色を変える

```html
<footer class="footer">
  <div class="footer-container">
    <p class="footer-logo">
      <img src="../img/kamocafelogo-1.png" alt="kamocafe">
    </p>
    <div class="footer-body">
      <nav class="footer-nav">
        <ul class="footer-nav-list">
          <li><a href="#about">about</a></li>
          <li><a href="#menu">menu</a></li>
          <li><a href="#photos">photos</a></li>
          <li><a href="#access">access</a></li>
        </ul>
      </nav>
      <p class="copyright">
        <small>
          &copy;Copyright 2021 <a target="_blank" href="https://twitter.com/camomile_cafe">@camomile_cafe</a>
        </small>
      </p>
    </div>
  </div>
</footer>
```

```css
.footer {
  /* 最小限の幅指定 */
  min-width: 95vw;
  margin: 0 auto;
  padding: 20px 0;
  background-color: #ca9253;
}

.footer-container {
  /* flexbox指定 */
  display: flex;
  min-width: 400px;
  max-width: 800px;
  margin: 0 auto;
  justify-content: center;
}

/* ロゴ配置の指定 */
.footer-logo {
  /* flexアイテムに最小幅、最大幅を指定する */
  /* flexアイテムの基本幅を指定する */
  flex-basis: auto;
  /* flexboxに余白がある場合、flexアイテムの伸び率を指定する */
  flex-grow: 1;
  min-width: 8vw;
  max-width: 18vw;
  margin: 0;
}

/* ナビゲーション/コピーライトの指定 */
.footer-body {
  /* flexアイテムの伸び率、縮み率、基本幅を指定する */
  flex: 0 1 auto;
  padding-top: 110px;
}

/* ナビゲーション自体に対する指定 */
.footer-nav {
  margin-bottom: 20px;
}

.footer-nav-list li {
  display: inline-block;
  margin: 0;
  border-left: 1px solid #fff;
}

.footer-nav-list li:first-child {
  border-left: none;
}

.footer-nav-list a {
  display: inline-block;
  padding: 0 15px;
  line-height: 1.2;
  color: #fff;
  text-transform: uppercase;
}

/* コピーライトの指定 */
.copyright {
  margin: 0;
  padding-left: 15px;
  color: #fff;
}

.copyright small {
  font-size: 11px;
}

.copyright a {
  color: #fff;
}
```
