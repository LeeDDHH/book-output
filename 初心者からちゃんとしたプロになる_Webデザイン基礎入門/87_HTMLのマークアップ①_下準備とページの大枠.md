# HTMLのマークアップ①_下準備とページの大枠

## データを収納するフォルダを作成する

## index.htmlのベース

```html
<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="">
    <title></title>
</head>
<body>
    
</body>
</html>
```

## ページ構造の確認とテキスト原稿の整理

```markdown
ヘッダー
  ロゴ画像
    
メインイメージ
  写真
    お茶が机の上にのっている写真
ナビゲーション
  ページ内の各コンテンツに移動するアンカーリンク
  about、menu、photos、access
メインコンテンツ
  about
    店のコンセプトを紹介する
      カモカフェは、高円寺に開店予定のカフェです
      
  menu
    パンの種類を紹介する
  photos
    イメージが湧くように写真で紹介する
  access
    店の連絡先と地図を掲載する
フッター
  ロゴと各コンテンツに移動するアンカーリンク
```

## head要素を編集する

```html
<meta name="keyword" content="夜,カフェ,お茶,睡眠,リラックス,東京都,カモカフェ,カモミール,カモミールティ,カモミールティー">
<meta name="description" content="日が沈んで夜眠るまでにリラックスするカフェカモカフェのホームページです。">
<title>カモカフェ</title>
```

## ヘッダー、メインコンテンツ、フッターの箱を作る

先にページの大枠となるヘッダー、メインコンテンツ、フッターをマークアップしておく

- ヘッダー
  - `header`
- メインイメージ
  - `figure`
- ナビゲーション
  - `nav`
- その他
  - `section`
- フッター
  - `footer`

```html
<body>
  <header>
    （ヘッダー）
    ロゴ画像
    #kamocafe
  </header>
  <main>
    <figure>
      （メインイメージ）
      [写真]
      お茶と紙と花の写真
    </figure>
    <nav>
      （ナビゲーション）
      * about（link: #about）
      * menu（link: #menu）
      * photos（link: #photos）
      * access（link: #access）
    </nav>
    <section>
      （about）
      #about
      カモカフェは睡眠にやさしいカモミールティーが楽しめるカフェです。
      仕事帰り、作業後の休憩、なんとなく誰かと話したい時などにぜひ立ち寄ってください。
      日が沈んでから店内でゆっくりと一息つきませんか。
    </section>
    <section>
      （menu）
      #menu
      ・カモミールティー ・・・ 300円
      ・ルイボスティー ・・・ 400円
      ・そば茶 ・・・ 300円
      ・黒豆茶 ・・・ 400円
    </section>
    <section>
      （photos）
      #photos
      [写真]
      （店内イメージの例）
      夜は、静かな空気の中で一日を振り返ったり誰かとちょっと話をしたりして過ごしたいものです。
      [写真]
      （テーブルにお茶が並んでいるイメージ）
      当店では睡眠に優しいノンカフェインのお茶が楽しめます。
      [写真]
      （teapeopleのネオンサイン）
      今夜、眠るまでにお茶を飲みながら過ごしてみませんか？
    </section>
    <section>
      （access）
      #access
      Caffeine-Free Drinks Tea Shop
      〒 123-4567
      東京都杉並区高円寺北 0-00
      TEL 012-345-6789
      [地図]
      Google map
    </section>
  </main>
  <footer>
    （フッター）
    ロゴ画像
    （フッターナビゲーション）
    * about（link: #about）
    * menu（link: #menu）
    * photos（link: #photos）
    * access（link: #access）

    &copy;Copyright 2021 @camomile_cafe
  </footer>
</body>
```
