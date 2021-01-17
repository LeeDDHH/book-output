# CSSの適用方法

## CSSをHTML文書に適用させる3角方法

- CSSファイルをHTMLファイルに読み込む
- HTMLファイル内にCSSを記述
- タグの中に属性としてCSSを記述

## CSSファイルをHTMLファイルに読み込む

```html
<!--
  rel：参照元ファイルとの関係
  href：参照元のパス
  -->
<link rel="stylesheet" href="style.css">
```

## HTMLファイル内にCSSを記述

## タグの中に属性としてCSSを記述

```html
<head>
  <style>
    h1 {
      color: #fff;
    }
  </style>
</head>
<body>
  <h1 style="background-color: #fe938c">サンプル</h1>
</body>
```
