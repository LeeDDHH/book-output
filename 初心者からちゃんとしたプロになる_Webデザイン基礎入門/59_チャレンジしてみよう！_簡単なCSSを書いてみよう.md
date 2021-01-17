# チャレンジしてみよう！_簡単なCSSを書いてみよう

[html-add-css](./html/html-add-css.html)

1. CSSファイルを作成する
2. CSSファイルを読み込む
    ```html
      <link rel="stylesheet" href="../css/style.css">
    ```
3. 文字コードを指定する
    ```css
      @charset "UTF-8";
    ```
4. 背景色をつける
    ```css
    @charset "UTF-8";

    h1 { background-color: #ffeb3b; }
    ```
5. うまくいかない突起のチェック事項
    ```markdown
    - スペルミス
    - 全角になっている
    - どこかに全角が入っている
    - `<link>` で読み込みしていない
    - `<link>` で読み込む祭のパスが間違っている
    - CSSファイルの保存場所が間違っている
    ```
