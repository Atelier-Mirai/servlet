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
