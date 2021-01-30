# HTMLのマークアップ②_各セクションを作り込む

ページの構造に応じて、 `大きな箱　→　小さな箱` とマークアップしたら、小さな箱の中身をマークアップしていく  
さらに小さな箱を作り、常に階層構造（箱の構造）を意識しながらすすめる

## ヘッダーをマークアップする

```html
<header class="header">
  <h1 class="logo">
    <img src="../img/kamocafelogo-1.png" alt="kamocafe">
  </h1>
</header>
```

## メインイメージをマークアップする

```html
<figure class="top">
  <img src="../img/debby-hudson-FO4gzqI2t84-unsplash.jpg" alt="お茶と紙と花の写真">
</figure>
```

## ナビゲーションをマークアップする

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

## 4つのセクションをマークアップ

各セクションにアンカーリンク先となるidを指定する  
各セクションの見出し部分は共通のデザイン

```html
︙
<section id="about">
  <h2>
    <img src="../img/about.svg" alt="about">
  </h2>
</section>
︙
<section id="menu">
  <h2>
    <img src="../img/menu.svg" alt="menu">
  </h2>
</section>
︙
<section id="photos">
  <h2>
    <img src="../img/photos.svg" alt="photos">
  </h2>
</section>
︙
<section id="access">
  <h2>
    <img src="../img/access.svg" alt="access">
  </h2>
</section>
︙
```

## 「about」セクションをマークアップする

セクションの見出しは `h2` で括る  
`img` タグでSVGファイルを指定する  
紹介文は `p` タグで括る

```html
<section id="about">
  <h2>
    <img src="../img/about.svg" alt="about">
  </h2>
  <p>
    カモカフェは睡眠にやさしいカモミールティーが楽しめるカフェです。<br>
    仕事帰り、作業後の休憩、なんとなく誰かと話したい時などにぜひ立ち寄ってください。<br>
    日が沈んでから店内でゆっくりと一息つきませんか。
  </p>
</section>
```

## 「menu」セクションをマークアップする

セクションの見出しは `h2` で括る  
`img` タグでSVGファイルを指定する  
メニューのリストは `ul` 、 `li` を使う

```html
<section id="menu">
  <h2>
    <img src="../img/menu.svg" alt="menu">
  </h2>
  <ul>
    <li>カモミールティー ・・・ 300円</li>
    <li>ルイボスティー ・・・ 400円</li>
    <li>そば茶 ・・・ 300円</li>
    <li>黒豆茶 ・・・ 400円</li>
  </ul>
</section>
```

## 「photos」セクションをマークアップする

セクションの見出しは `h2` で括る  
`img` タグでSVGファイルを指定する  
写真3点とキャプションを貼る

- 各写真とキャプションは `figure` で括る  
- 写真は `img` タグを使う
- キャプションは `figcaption` を使う

写真を一覧にして、リストとして扱うため、 `ul` で箱を作る  
箱の中は、3つの `figure` を `li` に入れる

```html
<section id="photos">
  <h2>
    <img src="../img/photos.svg" alt="photos">
  </h2>
  <ul>
    <li>
      <figure>
        <img src="../img/calm-place.jpg" alt="静かに過ごせるスペース">
        <figcaption>
          1日を振り返ったり、話し合ったりして寝るまでの時間を静かに過ごして見ませんか？
        </figcaption>
      </figure>
    </li>
    <li>
      <figure>
        <img src="../img/tea-and-table.jpg" alt="ノンカフェインのお茶、楽しめます">
        <figcaption>
          各種お茶、睡眠に良いものを用意しております。<br>
          カフェインを気にせず手元を温めながら香りも楽しんでください
        </figcaption>
      </figure>
    </li>
    <li>
      <figure>
        <img src="../img/tea-people-long.jpg" alt="お茶を楽しめる場所です">
        <figcaption>
          お茶を楽しむも、人と交流するも自由にお使いください
        </figcaption>
      </figure>
    </li>
  </ul>
</section>
```

## 「access」セクションをマークアップする

店名、連絡先（住所/電話番号）、地図を載せる  
連絡先（住所/電話番号）は `address` で括る  
店名、電話番号は意味を強調したいため、 `strong` で括る  
今回、地図はgoogle mapを使用する  
店名、連絡先と地図を左右横並びにするため、 `h2` 以外は `div` で囲む

```html
<section id="access">
  <h2>
    <img src="../img/access.svg" alt="access">
  </h2>
  <div>
    <address>
      <strong>
        Caffeine-Free Drinks Tea Shop
      </strong><br>
      〒 123-4567<br>
      東京都杉並区高円寺北 0-00<br>
      <strong>
        TEL 012-345-6789
      </strong>
    </address>
    <div>
      <iframe
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3239.848495741953!2d139.6499291!3d35.705345699999995!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x6018f27d700b2bdd%3A0xe2ef354e915f9930!2z6auY5YaG5a-66aeF!5e0!3m2!1sja!2sjp!4v1611969169166!5m2!1sja!2sjp"
        width="600" height="450" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false"
        tabindex="0"></iframe>
    </div>
  </div>
</section>
```

## フッターをマークアップする

ロゴ、ナビゲーション、コピーライトが入る  
ヘッダーと同じロゴを使用  
ロゴ画像は `img` で括り、さらに `p` タグで括る  
ナビゲーションは `nav` 、 `ul` 、 `li` 、 `a` を使う  
コピーライトは `small` で括り、 `p` で囲む  
横並びにするため、 `footer` の内側を `div` に囲い、さらに `nav` とコピーライトを `div` で括る

```html
<footer>
  <div>
    <p>
      <img src="../img/kamocafelogo-1.png" alt="kamocafe">
    </p>
    <div>
      <nav>
        <ul>
          <li><a href="#about">about</a></li>
          <li><a href="#menu">menu</a></li>
          <li><a href="#photos">photos</a></li>
          <li><a href="#access">access</a></li>
        </ul>
      </nav>
      <p>
        <small>
          &copy;Copyright 2021 <a target="_blank" href="https://twitter.com/camomile_cafe">@camomile_cafe</a>
        </small>
      </p>
    </div>
  </div>
</footer>
```
