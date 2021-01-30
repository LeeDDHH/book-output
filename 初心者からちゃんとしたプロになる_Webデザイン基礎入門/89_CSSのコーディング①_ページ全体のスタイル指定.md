# CSSのコーディング① ページ全体のスタイル指定

`全体共通　→　細かい部分`の順で指定していく

## リセットCSSを読み込む

地ならし作業  
リセットCSSを使ってWebブラウザの**初期スタイルのリセット**をする

- 各ブラウザの初期状態を統一する
- 各種ブラウザがすべて同じルールで表示できる用になる

[Normalize.css: Make browsers render all elements more consistently.](https://necolas.github.io/normalize.css/)

## ページや要素全体に適用するCSSを書く

HTMLの各要素に対して初期スタイルを設定

- 全称セレクタ（*）
- `body`

```css
* {
  /* padding、borderなどがwidthに加算されなくなる */
  box-sizing: border-box;
}

/* body全体に対して文字色、背景色、行送り、文字サイズ、フォントの指定 */
body {
  font-size: 16px;
  line-height: 1.5;
  font-family: -apple-system, BlinkMacSystemFont, 'Helvetica Neue', YuGothic, 'ヒラギノ角ゴ ProN W3', 'Hiragino Kaku Gothic ProN', Arial, 'メイリオ', Meiryo, sans-serif;
  color: #806341;
  background-color: sandybrown;
}
```

## 各要素の初期スタイルを指定する

ページ内で使う各要素に対して以下の設定をしておく

- `margin` 、 `padding` を `0` にする
  - 後の工程で行う細かなCSSスタイルの調整をしやすくするため
  - いったん指定しておけば、個々の要素に対して個別に余白を指定する

見出し、 `a` タグ、　`img` などページ内で共通に使う要素の初期スタイルを指定しておく

```css
/* 見出しの上下のmargin、行の高さを指定 */
h1, h2 {
  margin-top: 0;
  margin-bottom: 30px;
  line-height: 1.2;
}

/* リンクの文字色、文字の装飾を指定 */
a {
  color: #806342;
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}

p {
  margin-top: 0;
  margin-bottom: 1em;
}

ul {
  margin: 1em 0;
  padding: 0;
  list-style: none;
}

figure {
  margin: 0;
}

/* 画像の最大幅を指定 */
img {
  max-width: 100%;
  height: auto;
}

address {
  font-style: normal;
}
```
