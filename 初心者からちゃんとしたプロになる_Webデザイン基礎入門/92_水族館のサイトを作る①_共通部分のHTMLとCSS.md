# 水族館のサイトを作る①_共通部分のHTMLとCSS

## HTMLファイルのテンプレート化

- ヘッダー
  - サイトロゴ
  - ナビゲーション
- メインコンテンツ
- フッター
  - サイトのロゴ
  - 連絡先
  - SNSリンク
  - コピーライト

```html
<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="utf-8">
<title>Aqua</title>

<meta name="keywords" content="">
<meta name="description" content="">

<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
<meta name="format-detection" content="telephone=no">

<link rel="shortcut icon" href="img/favicon.ico">
<link rel="apple-touch-icon" href="img/apple-touch-icon.png">
<link rel="stylesheet" href="css/normalize.css">
<link rel="stylesheet" href="css/style.css">
</head>

<body>
<header class="header">
<!-- （ヘッダーを記述する） -->
</header>

<main>
<!-- （メインコンテンツを記述する） -->
</main>

<footer class="footer">
<!-- （フッターを記述する） -->
</footer>
</body>
</html>
```

ファビコン  

- `favicon.ico`
  - PC向け
  - 37x37px
- `apple-touch-icon.png`
  - スマホ向け
  - 180x180px

## 共通部分のHTMLとCSS①：ヘッダー

### ヘッダー

```html
<header class="header">
  <h1 class="logo">
    <a href="./index.html">
    <img src="img/logo.svg" alt="Aqua">
    </a>
  </h1>
</header>
```

```css
.header {
  /*
    ヘッダーの位置し指定
    メニューボタンの絶対配置の基準となる
  */
  position: relative;
  padding: 15px 0 0;
  background-color: #fff;
}

.logo {
  width: 140px;
  /* 中央揃え */
  margin: 0 auto;
  padding-bottom: 5px;
}
```

### ナビゲーション



```html
<input type="checkbox" name="navToggle" id="navToggle" class="nav-toggle">
<label for="navToggle" class="btn-burger"></label>

<nav class="nav">
<ul class="nav-list">
  <li>ホーム</li>
  <li><a href="guide/index.html" title=" 営業案内">営業案内</a></li>
  <li><a href="contact/index.html" title=" お問い合わせ">お問い合わせ</a></li>
</ul>
</nav>
```

```css
.nav-toggle {
  display: none;
}

.btn-burger {
  position: absolute;
  top: 5px;
  right: 10px;
  z-index: 2;
  display: block;
  width: 44px;
  height: 44px;
  background: url("../img/burger.svg") center center / 35px 20px no-repeat;
  cursor: pointer;
}

.nav-toggle:checked ~ .btn-burger {
  background : url("../img/close.svg") center center / 26px 26px no-repeat;
}

.nav {
  padding-top: 10px;
  background: url("../img/nav_bg.png") center center / cover no-repeat;
}

.nav-list {
  display: none;
  margin: 0;
  padding-bottom: 10px;
}

.nav-list li {
  margin: 0;
  padding: 10px;
}

.nav-list a {
  display: block;
  color: #fff;
}
```
