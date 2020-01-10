# 何をフィードバックしたらいいのか分からない

「どのソフトウェアにフィードバックするか」がはっきりしたら、次にはっきりさせるのは「何をフィードバックするか」です。

OSS Gateワークショップにビギナーとして参加される方は、「別に今何かOSSの使用上で困っているわけではないけど、OSS開発に関わりたい、OSS開発に関われる人になりたい」という人が多く、具体的に「これをフィードバックしたい」という情報を持っている人は少数派です。本書を読まれている方の中にもそういう人は少なくないでしょう。そこで本章では、「フィードバックするネタ[^feedback-point]」の見つけ方をご紹介します。これを読めば、あなたも明日からOSSへフィードバックするネタに事欠かなくなることうけあいです。

[^feedback-point]: OSS Gateワークショップでは、これを「フィードバックポイント」と呼んでいます。


## フィードバックできるネタは日常の中にある

といっても、べつにゲーム開発におけるデバッガー部隊のように「普通はやらない操作をとにかくいろんな組み合わせでたくさん試してみる」というような事をする必要はありません。するべきことはたった一つ、*OSSを普通に使う*ということです。ワークショップでも、「まずは普通に使ってみる」というステップに半分くらいの時間をあてています。

ただし、そのときには*使っている途中で遭遇した些細な「つまずき」を見落とさない*ことが大切です。何が「つまずき」なのかピンと来ない、「普段からOSSを使っていて、べつにつまずいたことなんて無いんだけどな……」という人は、ちょっと立ち止まって考えてみてください。それは*あなたが「自分がつまずいたという事」自体に気付いていない*だけなのかもしれません。「そんなバカな！」と思いますか？　では、以下のような話に身に覚えはないでしょうか。

* 書かれているとおりの手順でインストールしたが、失敗した。ググったら、◯◯というパッケージを先に入れておかないといけないと書いてあるブログが見つかった。
* どこから始めればいいか分からなかったので、「（機能の名前） 使い方」でググってQiitaやStack Overflowや個人のブログの解説を参照した。
* コマンドを実行しようとしたら、初期設定をして下さいというメッセージが出てエラーになった。もう1度起動したらエラーが出なくなった。
* 機能を実行しても何もメッセージが出なくて、ちゃんと動いたかどうかよく分からなかった。ファイルの方を見たら、実はちゃんと保存されていた。

どうでしょう。「いつもの事だから、特別つまずいたとは思っていなかった」「そんな事でいちいち立ち止まってたら仕事にならないし」と思う人もいるのではないでしょうか。

何かする度につまずくというのはストレスになり、ストレスに意識して向き合うのは疲れるものです。また、よくつまずくのは自分の技術力が低いことの表れだと考えるなら、つまずきを意識するのは自分の無能さと向き合うということで、それもまた辛いものです。そもそも、そのOSSを使って本来やりたいことが別にあったわけで、それと無関係なことに時間を取られること自体煩わしいでしょう。なので、誰もがつまずきを意識しないような*鈍感力*を身に着けてしまいがちです。ですが、*OSSにフィードバックするにはこの鈍感力が邪魔になる*のです。


## 「注意が必要な点」で終わらせるのはもったいない

本書を読まれている方の中には、すでに積極的に情報をアウトプットしているという人もいるかもしれません。改めて言うまでもなく、アウトプットすることは技術力を養う・成長するために有効です。例えば以下のようなやり方を取っている人は多いでしょう。

* 社内のWikiなどにメモを書いて、他のチームメンバーに情報を共有する。
* Qiitaや社外向けのブログに記事を書いて、広く一般に情報を公開する。
* 同様のノウハウを集めて本の形にして、技術書典のような場で同人誌として頒布する。

ところで、そこでアウトプットしているのはどんな情報でしょうか？　*普通に使おうとしてつまずいたことについての注意点やノウハウ*を述べている場合、フィードバックのチャンスかもしれません。

実際の事例を一つご紹介しましょう。Webページ上でマウスカーソル（ポインタ）をかざした位置の語句を辞書で引いて結果をポップアップ表示する[「Mouse Dictionary」というGoogle Chrome用の拡張機能](https://mouse-dictionary.netlify.com/en/)について、インストールして使い始めようとしたらポップアップが真っ白になってしまう、という問題がありました。色々調べてみた結果分かったのは、この拡張機能は使い始める前に初期設定が必要で、初期設定が済んでいないと辞書を引けないためにこの問題が起こるということでした。

（改善前の様子のスクリーンショット）

「この拡張機能は有用なので、他の人にも紹介したい」と思っても、これでは使い始めたときにかなり高い確率で同じ問題に遭遇することになると予想できます。ブログなどで紹介するなら、*「このソフトウェアを使う時はこのような点に注意が必要です」というノウハウ*を添えて紹介した方が良さそうです。実際、様々なソフトウェアについてそのような紹介記事が存在しています。

ですが、冷静に考えてみて下さい。この拡張機能を使い始めた人が高確率で戸惑うであろう注意点は、注意するべき点と言うよりも*不具合*や*不備*と言った方が適切ではないでしょうか。例えば、真っ白なポップアップの代わりに「初期設定をする必要があります」といった注意喚起のメッセージが表示されるようになっていれば、戸惑う人はいなくなるでしょう。そこで、そのような改善案を[公開されているGitHub上のイシュートラッカーで提案](https://github.com/wtetsu/mouse-dictionary/issues/19)してみました。すると、提案を有用と判断してもらえて、次のバージョンで改善が図られることになりました。つまり、*ソフトウェアを使う上で特別な注意が必要ない状態*になったのです。

（改善後の様子のスクリーンショット）

ノウハウの言語化・文書化は有意義ですが、OSSに関わりたいと考えている人は、ぜひそこから一歩先に考えを進めてみて下さい。*「使う時に特別な注意が必要ないのが一番いい」、これはどんな場合にも言える事です*。この考えを持っていれば、「使用上の注意点」はおのずと「改善した方がよい点」に見えてきます。


## 使い始めこそフィードバックのチャンス！

このようなインストール手順などの使い始めの時期に遭遇するつまずきは、「普通に使う過程でのつまずき」の代表です。OSS Gateワークショップでもよく見られ、先の例もまさに[株式会社アカツキさんの社内で実施したOSS Gateワークショップ](https://www.clear-code.com/blog/2019/5/29.html)の中で実際に行われたフィードバックの事例でした。

謙虚な人は、つまずきに遭遇した時に「つまずいたのは自分の勉強が足りなかったからだ、豊富な知識があればつまずく前に気がつけたはずだ」「こんな所でつまずくのは初心者だけに違いない、こんな所でつまずいたと人に知られるのは恥ずかしい」と考えるかもしれません。確かに、こういうつまずきを難なく乗り越えられるのも技術力があるということの証と言えます。ですが、*つまずきに気がつけるかどうか、つまずきをつまずきとして意識できるかどうかは、それとは別の話*です。

謙虚に学ぶ姿勢は大事ですが、ここは*一旦謙虚さを忘れて、自分の気持ちに素直になって「どうだったら嬉しかったのか」を考えてみましょう*。つまずいたのは「自分のレベルが低いから」ではなく「ソフトウェアに問題があるから」「説明が足りないから」ということはないでしょうか？　「つまずいたのは自分の勉強不足のせい」「こんな所でつまずいたと人に知られたら恥ずかしい」という考え方は一旦封印しましょう。むしろ、「*つまずいた自分じゃなく、こんな最初の方につまずくような部分が残ってる事の方が悪い*」と考えてもいいくらいです。そういう視点で「つまずき」を「どうだったらよかったか」と表現してみましょう。例えばこんな感じです。

* インストール手順の説明の中に必要な前提が書かれていなかったのでつまずいた。
  →必要なパッケージがあるなら、最初からそれも手順に書いておいたり、自動的にインストールするようになってくれていたりすればいいのに……
* コマンドを実行しようとｓしたら、初期設定をして下さいと言われてエラーになった。
  →初期設定が必須なら、インストール手順の中に書いてあればいいのに……
* 機能を実行しても、ちゃんと動いたかどうかよく分からなかった。
  →動作確認の方法も書いてあればいいのに……

ほら、今までストレスでしかなかったものが、改善できそうな点に見えてきましたね。*これを開発元に報告したり直したりしていくこと*、それがOSSへのフィードバックなのです。

多くの小規模なOSS開発プロジェクトでは、インストール手順や使い方の説明などのドキュメントの整備には手が回らなくなりがちです。というのも、1回使い方を習得した人はこの手の情報をそうそう見返さないため、習熟度が高まれば高まるほど「かかる手間のわりには自分自身が恩恵を受けられない」ことになるからです。また、用意するときもどこまで細かく書けばいいか分からず、言葉足らずな内容になってしまいがちです。

しかし、使い始めるのに注意や知識が必要な状態だと、「既にわかっている人」以外にとってそのOSSはどんどん使いにくく・関わりにくくなってしまいます。そうすると、新規のユーザーや開発者が増えない一方で、それまで関わっていた人達はライフステージの変化などにより「卒業」していき、最終的には新機能の追加も無ければ脆弱性の修正も無く誰にもメンテナンスされないままの、見捨てられたプロジェクトになってしまいます。そうなって一番困るのは、一般のユーザーです。「導入しやすくする」「不親切な案内を丁寧な内容に直す・補完する」という改善もプロジェクト自体の長期的な継続のためには欠かせず、だからこそ、*新たに使い始めて実際につまずいた人からのフィードバック*は非常に有用なのです。


## 常につまずきに敏感でいよう

OSSを導入した後もつまずきは日々発生します。つまずいたままではどうにもならないので、ググったり試行錯誤したりしてつまずきを回避する、という日常を多くの人が送っていることでしょう。そういう時に、その都度開発元にフィードバックできればベストなのですが、最初のうちは「よし、やるぞ！」と気合いを入れて臨まなければ「フィードバックするモード」に頭を切り替えられないかもしれません。スケジュールの都合などで、すぐにフィードバックするのは難しいという場合も多々あると思います。

そんな時は、無理に一気にフィードバックしなくても構いません。ただ、*つまずいた事に敏感に気付くようにして、つまずきを忘れないように記録を残しておく*ようにしてください。そして、「毎週月曜日の17時から2時間」のようにタイミングを決めて、残したメモを元に実際にフィードバックしてみるようにし、「フィードバックする」ということ自体を習慣化するといいでしょう。そうして少しずつ機会を重ねていく中で「あれっ、フィードバックするのに30分もかからなかったぞ？」と気がつけばしめたものです。そうなればもう「定期的にフィードバック」する必要はなく、つまづいた時に即フィードバックできるようになっているはずです。

「OSSへフィードバックするって、何か特別な事だ」「そんな事ができるのは別の世界の人だ」と思っていましたか？　フィードバックは決して特別な事ではなく、このように日常の延長線上にある物なのです。皆さんも、OSSを使っていて遭遇した些細なつまずきをきっかけに、フィードバックに挑戦してみてください。