# 初学者の方へ

## 物語のあらすじを掴みましょう
書籍を読まれる際、あらすじを掴むことは、 全体を理解する上で有益です。
まずは大まかに流し込みを行い、あらすじをつかみましょう。
どのような登場人物が現れるのか、全体の鳥瞰図を作成しましょう。
鳥瞰図は、個々の詳細を把握することはできませんが、全体を俯瞰してみることができますので、おおまかな全容の把握に役立ちます。

竹取物語で言えば、竹から生まれたとても美しいかぐや姫が、五人の若者や帝からも求婚されますが、月に帰ってしまうお話です。
あらすじを掴んだら、五人の若者に何を求めたのか、 この物語から汲み取れることは何かなど、思索を深めていきます。

コードが現れると、「どういう意味だろう？」と 考えたくなりますが、「後から詳しく読むから待っていてね」と、まずは一旦棚上げして、物語のあらすじを掴むことに専念しましょう。
物語のあらすじを掴んだら、少し高度を下げて、個々の詳細を把握していきましょう。
## 登場人物を把握しましょう。
竹取物語での登場人物は、大きく分けて、かぐや姫と求婚者たちでした。  

サーブレットJavaでの登場人物は、
大きく分けると、  
１）クライアント（顧客）と成って、画面表示を担当するHTML, JSPファイル達  
２）サーバー（給仕者）と成って、顧客の要求（リクエスト）に応じて、さまざまな応答（レスポンス）を返す Servlet  
が登場します。

喫茶店で、コーヒーを注文するときを想像して下さい。
１）クライアント（顧客）は、「コーヒーを下さい」と要求（リクエスト）します。  
２）サーバー（給仕者＝ウェイター、ウェイトレス）は、「ご注文のコーヒーです」と、応答（レスポンス）を返します。  

ウェブアプリの開発でも同様です。
１）クライアント（ブラウザ=Chrome）は、「index.html」を見せて下さいと、ウェブサーバーに要求（リクエスト）します。  
　　(ブラウザのアドレスバーに、http://localhost:8080/index.html と入力してエンターキーを押すことに相当します)  
２）ウェブサーバー（=tomcat）は、「ご注文のindex.htmlファイルです」と、クライアント(ブラウザ)に応答（レスポンス）を返すので、
受け取ったクライアントは美味しくコーヒーを飲みます（htmlを解釈して画面表示します）

## Eclipse(月蝕)
Java基礎は、さくらエディタで開発しましたが、サーブレットJavaでは、Eclipseという統合開発環境(IDE)を使っています。
Eclipseは多機能です。ファイルの編集はもちろん、Javaファイルのコンパイルや、簡易ウェブサーバーであるTomcatの起動等もできます。

１）クライアント（顧客）と成って、画面表示を担当するHTML, JSPファイル達は、WebContent以下に配置します。  
２）サーバー（給仕者）と成って、顧客の要求（リクエスト）に応じて、さまざまな応答（レスポンス）を返す Servlet 達は src以下に配置します。  

## 完成形を見てみましょう。
http://localhost:8080/index.html/sample/dao/login.html  がそれです。  
ID: taro, PW: hitachi でログインできます。趣味などをいろいろ登録できる機能があります。  
クライアント側（画面表示担当）でいろいろデータを入力する。  
サーブレット側（制御色々担当）では、クライアントから入力されたデータを受け取り、  
　　データベースに照会(select文したり)、照会結果を加工したりなど、  
　　いろいろ処理して、結果をクライアントに返す。  
ことをやっています。
サーブレットで処理したデータを、クライアントに返すために、リクエスト属性やセッション属性を使ったりします。

## 楽しみましょう( ◠‿◠ )
宇宙絶対の真理が書かれている書籍ではありません。
Java基礎の時には、文字が表示されるだけでしたが、
ウェブの世界になると、色もつくようになりましたし、絵も出るようになりました。
いろいろなボタンを押すと、それに応じて、応答もしてくれます。
インタラクション、対話ができます。
少し肩の力を抜いて楽しんでみて下さい。

## おまけ
画面表示が少し殺風景で寂しいと感じる方もいらっしゃるかもしれません。
common.css の二行目から五行目に以下を追記しましょう。

* 画面が桜色になり、入力枠やボタンも装飾がついて楽しくなります。
```css
@import "https://cdn.jsdelivr.net/npm/sakura.css/css/sakura.css";
body { 
    background: #feeeed; /* 桜色 */
}
```


* Eclipse(月蝕)に因んで、青白い月の光の雰囲気を楽しみたい方に。
```css
@import "https://unpkg.com/mvp.css@1.15.0/mvp.css";
body {
    background: #eaf4fc; /* 月白 */
}
```


* 風薫る皐月の空と緑さす新緑のイメージならこちらを。
```css
@import "https://cdn.jsdelivr.net/npm/water.css@2.1.1/out/water.min.css";
body {
    background: #e0ebaf; /* 若芽色 */
}
```



##  ウォーターフォールモデルについて
「さくらマーケット」というネットショップの開発を行っていきます。
ウォーターフォールモデルという開発方法があります。
ちょうど、滝が上から下へ流れ落ちるように、
「要件定義」「設計」「開発（プログラミング）」「テスト」「運用」というそれぞれの工程を経て一つのプロジェクトを達成していきます。

## MVC について
Java基礎やサーブレットJavaで習得した技術を活かして、「開発（プログラミング）」工程はこなせることと思います。
表示を司る「ビュー(html, jsp)」、制御を司る「コントローラ（サーブレット）」、ビジネスロジックを司る「モデル（データの登録等）」を意識すると、開発しやすいです。サーブレットJavaで学習したコードも流用することができます。
## テストについて
テストは、Java基礎の総合演習で、driverと呼ばれるコードとして登場しました。小さなプログラムであれば、手動で動作確認することもできますが、何度も何度も繰り返し確認するのは大変ですし、元のプログラムコードを変更する都度、動作確認するのはとても労力がかかる作業になります。そこで登場するのがテストコードと呼ばれる動作確認を行うためのプログラムです。このテストコードがあることにより、元のコードを変更したら動かなくなるんじゃないだろうか？ と不安を感じることなく、自信を持って元のコードを編集できるようになります。元々のコードをより簡潔で見やすく美しいコードへと改善できるようになります（リファクタリングと言います）。また、どのようなテストを行ったのか、テストコード自身が物語ってくれますので、書かれたコードの品質に自信を持つことができます。

## ドキュメントについて
実際に作られたプログラムは大抵の場合長く使われることになります。運用していく中で、数年後に機能追加等をする際に、仕様を確認したくなるかもしれません。自分で作ったプログラムであれば、しばらくの間は覚えていることでしょうし、何ヶ月か経ったとして忘れていてもコードを読み直し思い出すこともできます。そして全く見たこともない会ったこともない方が頼れるのはドキュメントのみです。百行のコードであれば読んで理解することもできますが、百万行のコードを理解するのは至難の業です。未来の技術者に宛ててのメッセージ、玉手箱です。素敵なドキュメントを残しましょう。
## スケジュールについて
「要件定義」「設計」「開発（プログラミング）」「テスト」「運用」という五つの工程の中で、「開発（プログラミング）」が占める部分は実はほんのわずかです。「運用」は完成してから行われますので除外するとして、単純に割り算しても１／４になります。物事は想定したようにはいかず、遅れが生じることもあるでしょう。スケジュールに余裕がないと精神的にも辛いことになります。「さくらマーケット」はどれくらいの期間で完成できると見積もりますか？ 予備日も含めて、ざっくり１／５くらいでみてもいいかもしれません。
## みんなで創りましょう
プログラミングが得意な人もいれば、そうでない人もいるかと思います。もしかすると、プログラミングが得意な人が全部創ってしまった方が速くできるかもしれませんね。
「全然コード書けなくて、エクセル係してました〜。せっかくJava学んだから、ちょっとだけでもやりたかった・・・」って寂しい思い、悲しい思いはして欲しくないのです。
みんなでいいもの作ろうっていろいろ議論して、アイディアを出し合って、そしてみんなの力を合わせて「出来た〜！ 完成！」って、グループみんなですごい課題を成し遂げた 「勝利した！」「達成した！」って喜んで欲しいです。

Javaに触れるのはこの研修が最後という方もいらっしゃるかもしれません。現場で開発に携わる方でも「要件定義」〜「テスト」までの一連の流れを疑似体験できる機会は貴重です。


個人的には、たとえ小さな一つの機能であったとしても「このログイン機能は、HTMLも書いてJavaも書きました。データベースもやったし、テストもしました。ドキュメントも作りました。わたしの作品です！」って胸を張れるほどに愛おしくなるほどに、創って欲しいです。それがきっと輝く未来を生きるあなたの財産になると思うから。

どうぞ、みんなで楽しんで素晴らしい作品を創り上げてください。そして、勝利と達成の美酒を味わってください！
```
