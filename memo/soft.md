「やさしい言い方」の話


これを書くまで僕は思いもしてなかったんだけど、「コードレビューで優しい言い方を心がけて」というのは人によっては「こちらの変数定義ですが、僭越ながら私めには不要なように思えるのですがいかがでしょう？」みたいなのを誇張でなく本気で想像してたりするんでしょうか？

僕はこの手の話は
「なんでこんな無駄な変数定義してんだよクソだろこのクソ忙しい時にクソ下らねえ事で時間取らせてんじゃねえよ何考えてんだ脳味噌腐ってんじゃねえの」
を
「この変数定義は不要なので削除した方がいいですね」
と改めましょう、というような話だとずっと思ってたんですが。

そこまで極端じゃなくても
「この行、無駄。消せ。（理由は言わんでも分かるだろ、わかんないならお前が悪い。いちいち言わせんな。とムスっとした表情で言う）」
を
「この変数定義は不要なので削除した方がいい」
に改めましょう、くらいのことは全然普通にありそうな気が僕はしています。

心理的安全性の話の時に僕は
「この行、無駄。消せ。（ムスっとした表情で）」
みたいな殺伐とした空気の場所で並の人が萎縮せず安心して働けるとは思えないと考えて「言葉遣いも大事なのでは」と書きましたが、そのときに「優しい言葉遣いは心理的安全性の範疇ではない」的な事を言われたと感じました。

あの時「言葉遣いは重要じゃない」的な事をおっしゃった人はもしかして、
「この変数定義は不要なので削除した方がいいですね」
を
「これ、消していいんじゃないかと……いや、うん、そうですよね、これも大事ですよね、あはは～……」
にせよと僕が言っていたとでもお思いだったのでしょうか？

もしそうなんだったら話が通じる訳がないなと思ったんですが。どうなんでしょうか、「心理的安全性に言葉遣いの優しさは不要」派の方々的には。

人間関係を円滑にとかそういうのどうでもいいから技術的正しさ最優先で
「この行、無駄。消せ。（ムスっとした表情で）」
が許される状態を作るのが真の心理的安全性だ、ということであればやっぱり僕は心理的安全性には関わりたくないなと思う感じです。

「この行、無駄。消せ。（ムスっとした表情で）」
と
「この変数定義は不要なので削除した方がいいですね」
の間に違いはまったく無い、と感じる人でないとITエンジニアになれない・なるべきでない、とは僕は思わないです。

でも
「この変数定義は不要なので削除した方がいいですね」
と言われて傷付いたいじめられた！！と騒ぐ、
「これ、消していいんじゃないかと……いや、うん、書いた君の気持ちも大事だよね、あはは～……まあ君が決めていいよ」
と言われないと嫌だ、という人はITエンジニアに向いてないとは思います。

レビューの技術的判断に手心を加えて技術的な正しさを放棄するかどうかと、その判断の伝え方を剥き身の刃にするかマイルドにするかは別の問題だ、と僕は考えています。

まさかITエンジニアを自認していて経験も豊富な人が、そんな事の区別すらも付かないほど愚かな訳ありませんよね？（←剥き身の刃）

いや僕今結構感情的になってる自覚あるんですよ。
「ええっもしかしてそんな事も考えないで言葉使いが優しい優しくないを論じてた訳？　言葉の表現に対する理解の解像度低すぎない？　そんな解像度で物を言ってたの？！」
って。困惑していてその困惑をもてあましてる。

極端な話、「あーこの子は豆腐メンタルだから正しいか正しくないかで話しちゃ駄目だよ、この子に優しいか優しくないかだけ考えなきゃ駄目だよ、そうだよね～よちよち」と「技術的な正しさを放棄し、それを剥き身で言う」組み合わせだってある。

そんな感じで考えてるので、「ボロクソに貶されても涼しい顔をしてられる」 https://twitter.com/nida_001/status/1196400704283242496 は必ずしも長所とも言いきれ
ないと思う。自分に向けられる刃に無頓着な人が、人に向ける刃に無頓着でないとは僕には思えないので。

とりあえず今回、「優しい言い方」という表現ひとつ取っても人によって受け取り方に大きな幅があって、具体的にイメージしている物があるならちゃんと具体例を添えた方がいいよねというのは、自分も思いました。そこのコストをケチると解釈が分かれて話がわやになる。


も、そのように考えられるようになって以降は、より有用な報告ができ、提出したパッチやプルリクエストを取り込んでもらえる機会も増えたように思います。まだOSSの開発への参加に不慣れで、報告がうまくいかなくて悩んでいるという方は、この記事で述べた点を意識してみてはいかがでしょうか？

また、この記事で述べた事は実際にはOSSに特有の話ではなく、一般的に企業内でバグ票をやり取りするような場合にも共通して言える事です。[1つ前の記事](20190618)ではOSSのイシュートラッカーを出入り自由の社屋や工場にたとえましたが、OSS開発の場で広く共有されているノウハウの中には、普通に仕事の上で有用な物も多く含まれています。特に、OSS開発では「多くの人を雇って人海戦術で乗り切る」というような力業での解決が難しいため、いかに少ないコストで最大の効用を得るかという点で工夫がなされている事も多いです。

