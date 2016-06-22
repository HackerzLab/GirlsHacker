# embed_sns - ツイッター、フェイスブックを埋め込む方法

    ツイッター公式のヘルプを参照

    https://support.twitter.com/articles/20171533

    これらを実行するにはツイッターのアカウントを持っている事が前提

    手順

    右上の自身のアイコン > 設定 > ウィジェット

    ウィジェット > 新規作成 > 検索
    検索クエリに hackerz_hkt

    ウィジェットを作成

    入力フォームにハッカーズのツイッターURL を入力
    https://twitter.com/hackerz_hkt

    埋め込みコードが発行されるのでコピーする

    <a class="twitter-timeline"  href="https://twitter.com/search?q=hackerz_hkt" data-widget-id="744889308679544832">hackerz_hktに関するツイート</a>
    <script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0],p=/^http:/.test(d.location)?'http':'https';if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src=p+"://platform.twitter.com/widgets.js";fjs.parentNode.insertBefore(js,fjs);}}(document,"script","twitter-wjs");</script>

    早速貼り付けてみる

-----

    フェイスブック

    フェイスブックデベロッパー
    https://developers.facebook.com/


    ドキュメント > ウェブ開発者 > ソーシャルプラグイン
    https://developers.facebook.com/docs/plugins

    ページプラグイン
    https://developers.facebook.com/docs/plugins/page-plugin

    FacebookページのURL に
    https://www.facebook.com/TrainingHackers/
    を入力 コードを取得をクリック

    IFrame をクリックしコードをコピーする
    <iframe src="https://www.facebook.com/plugins/page.php?href=https%3A%2F%2Fwww.facebook.com%2FTrainingHackers%2F&tabs=timeline&width=340&height=500&small_header=false&adapt_container_width=true&hide_cover=false&show_facepile=true&appId" width="340" height="500" style="border:none;overflow:hidden" scrolling="no" frameborder="0" allowTransparency="true"></iframe>

-----

    コード張り込む場合行数をすくなくするために長く記述していますが、
    これは改行文字などを極力するための工夫でもあり、埋め込みコードではよく使われるやり方です。

    この埋め込みコードがなにをやっているか改行をふやして、みてみましょう

-----

・ツイッター埋め込み

```html
    <!-- ここは a タグのリンクです -->
    <a class="twitter-timeline"
        href="https://twitter.com/search?q=hackerz_hkt"
        data-widget-id="744889308679544832">hackerz_hktに関するツイート
    </a>
    <!-- ここから javascript の記述です -->
    <script>
    !function(d,s,id){
        var js,
        fjs=d.getElementsByTagName(s)[0],
        p=/^http:/.test(d.location)?'http':'https';

        if(!d.getElementById(id)){
            js=d.createElement(s);
            js.id=id;js.src=p+"://platform.twitter.com/widgets.js";
            fjs.parentNode.insertBefore(js,fjs);
        }
    }(document,"script","twitter-wjs");
    </script>
    <!-- ツイッターは html の a タグと js のコードでタイムラインを取得しています -->
```

・フェイスブック埋め込み

```html
<!-- html の iframe タグを使って埋め込みを行っています -->
<iframe
    src="https://www.facebook.com/plugins/page.php?href=https%3A%2F%2Fwww.facebook.com%2FTrainingHackers%2F&tabs=timeline&width=340&height=500&small_header=false&adapt_container_width=true&hide_cover=false&show_facepile=true&appId"
    width="340"
    height="500"
    style="border:none;overflow:hidden"
    scrolling="no"
    frameborder="0"
    allowTransparency="true">
</iframe>
<!-- width, height で大きさが変更できるようです、試しにやってみましょう -->
```

## 最近の web サイトの傾向としては

    スマートフォンの普及によって、いまどきの web サイトは大抵スマホ対応
    今日紹介した、レスポンシブルデザインを採用する事が多くなっています。
    一昔前は、HTML, CSS, JS, を一から組み上げてこのような凝った web サイトを
    作り込んでいましたが、最近は、 Bootstrap のような既存のフレームワーク
    と呼ばれるものを活用する事が多くなってきました。

    twitter や Facebook に代表される SNS と呼ばれるものを
    web サイトに埋め込んで表示するやり方もよく使われるやり方です。

    web プログラミングの世界もどんどん進化して、あまりプログラミングの知識に
    明るくない方でも、すでにあるフレームワークなどを上手く活用すれば
    それなりのものが手軽に作れるようになりました。

    しかしながら、人間の欲求はとどまる事をしりません。

    既存のフレームワークなどに存在しないものを欲しくなった時、
    または、人から要望された場合、これらの web サイトがどのような仕組みで
    実現しているのかを理解しておくと、とても便利ですね。

    次は今の web ブラウザには必ず搭載されているであろうクッキー (cookie) を紹介しながら
    プログラミングの世界にふれてみましょう。
