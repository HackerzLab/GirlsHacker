# embed_text - コンテンツを埋め込む手順

    index_test.html にあらかじめ用意しておいた
    テキストデータを埋め込んでいきましょう。

    一つづつ埋め込んだ後、web ブラウザーをリロードして、
    どう変化していくか確認しながら進みましょう。

    埋め込む内容は content.txt に用意してあります。

    手順

    1: <html lang="en"> を <html lang="ja"> に張り替えます
        これはこのページが日本語 (japan) ですと明言するためのものです
        表示は変わりませんが、検索される場合や音声読み上げの正確性が上がります。

    2: <title>Bootstrap 101 Template</title> を <title>Hackerz Lab.博多</title>
        に変更します。
        web ブラウザーのタブの部分の表示が変わります。

    3: 外枠をつくります
        http://getbootstrap.com/examples/theme/ を参考にして部品を活用します。
        Theme example と書いてあるようなデザインを組み込みます。
        <body> を <body class="container"> に置き換えます。
        Hello, world! の両脇に空白ができます。
        class 要素に container を宣言することで、画面の大きさに応じて
        レイアウトが変化するベース部分ができます。

    4: 見出し jumbotron を採用します。
        <h1>Hello, world!</h1> を
        <div class="jumbotron">
          <h1>Hackerz Lab.博多</h1>
          <p></p>
        </div>
        に変更します。 見出しができました。

    5: 見出しの説明文をつくります。
        <p></p> を #5 の内容に置き換えます。

    6: Thumbnails と Wells を使ってこのサイトの簡単な説明文を作成します。
        <div class="jumbotron">
        ...
        </div>
        の下に #6 を埋め込みます
        class="row" は一行にまとめる
        class="col-sm-3"
        class="col-sm-9"
        3/12 9/12 の割合になる

    7: Panels を使ってイベント告知をつくります。
        #7 を埋め込みます

    8: List groups を使って、当日の流れをつくります。
        #8-1 を埋め込んでリストの外枠をつくります。
        #8-2 を <li class="list-group-item active">16:00 開場</li> の下に埋めこみます。
        #8-3 の原稿を #8-2 を参考にして埋め込みます。

    9: Labels と Panels を組み合わせて 申し込みの案内をつくります。
        #9 を埋め込みます。

    10: Panels をアコーディオン形式の開く、閉じる、パネルで更新情報をつくります。
        #10 を埋め込みます
        このままでは動きがありませんので、
        <h3 class="panel-title">更新情報・お知らせ</h3>
        を #10-1 に書き換えます
        <div class="panel-body">
        を #10-2 に書き換えます

    11: Alerts を使って、注意事項を目立つようにします。
        #11 を埋め込みます

## これで基本的なコンテンツがそろいました、次はさらにコンテンツを充実させます
