#　2 開発のはじまり（7月初旬）

## 気軽にはじめてしまった
 ヴァイブコーディングについてはあまり調べなかった。ChatGPTにやりたいことを気軽に頼んでみることにした。まずは自分の作りたいものを書く。そのために、どういうアプリがあったらうれしいかを考えた。これはつらつらと人間が考えています。そしてそれをまとめ、実現するための手順を聞いた。
<img src="images/02_1st_dev-2025-10-12-15-47-02.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">


すぐ返事が返ってくる。

 <img src="images/02_1st_dev-2025-10-12-15-48-05.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">

 <img src="images/02_1st_dev-2025-10-12-15-49-01.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">

 <img src="images/02_1st_dev-2025-10-12-15-50-15.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">


 いや、フェーズとか言われても……。えっこんなに本格的なの。ちょっと待て。ここは正直にこちらのスキルを伝えなければ。
 

<img src="images/02_1st_dev-2025-10-12-15-51-37.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">


  ミニゴールっていいですね。じゃあやってみるかな。
  相談して最初に作ってみようといわれたのがこれ。
 <img src="images/02_1st_dev-2025-10-12-15-53-17.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">

  
## 初めてのAPI
 おおーAPIがでてきた！　憧れのAPI！　API叩けるようになったらなんでもできるぞ！
 もちろんAPIなんて使ってみるのは初めてなので、APIの使い方を逐一聞きながら進める。
 HTMLファイルも出してもらってローカルに保存、ブラウザで表示すればいいらしい！
 <img src="images/02_1st_dev-2025-10-12-16-14-42.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">

 
が！動かない！
<img src="images/02_1st_dev-2025-10-12-16-15-39.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">


 先に言えや！！！
 
<img src="images/02_1st_dev-2025-10-12-16-16-37.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">


ほんとだな。じゃあおすすめにします。

## 初めてのサーバー立て
 ChatGPTのいうことにゃ
<img src="images/02_1st_dev-2025-10-12-16-19-34.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">

 まあそうですよね。サーバーたてなきゃ動かないよね。
 しかし5分てどこから来たのか。気軽に言うが、言われたとおりやっても動かない。このあたりからだんだんChatGPTの「5分でできます！」はあやしいと思い始めてきた。動かないといったら「Windowsだとだめかも」という。方法を聞いたら別のコマンドを教えてくれた。幸い私はpythonを入れてあったので起動した。
<img src="images/02_1st_dev-2025-10-12-16-23-58.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">


 
  
## 初めてのエラーつぶし
  ChatGPTと開発していくときに欠かせないのがエラーつぶしだ。というかこれが主かもしれない。
  いわれるがままにここまで進めてきたが、開発らしきものをやっていくとなるとここがポイントらしいということがうすうす見えてきた。

  1. うまくいかないことをChatGPTに人間が伝える
  2. エラーの確定をするための方法をChatGPTが指示
  3. 人間がそれを実行して結果をChatGPTに教える
  4. ChatGPTが修正案を出し、それをまた人間が実行
  5. うまくいくまでくりかえし

  ファイルを作り、指定のところに置いて実行してアクセスしてみるが、まあ思った通りには動かない。次に指示されたのが「ブラウザ開発者ツールを開いて確認せよ」。もちろん、ブラウザ開発者ツールも使ったことないので、開き方から見方まで全部聞く。
  しかしまだ解決できない。エラーを究明するためにログを出させるコードも修正してほしいと言ってきた。こういうやつ↓
  <img src="images/02_1st_dev-2025-10-12-16-38-27.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">

  <img src="images/02_1st_dev-2025-10-12-16-39-01.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">

  
 とにかく、いわれたままにコードを人間が書き換え、実行して結果を伝えます。
<img src="images/02_1st_dev-2025-10-12-16-40-04.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">

 ほめてくれてありがとう。んでもってこれを修正するためのコードがでて、書き換えて、というのをがんばっていきました。

## API利用開始トラブルの解決
 <img src="images/02_1st_dev-2025-10-12-16-41-12.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">

 きりがない……。
 こんな感じで延々続くエラーをつぶしていきます。API使うのたいへんですね。
 結局の結論は。
 <img src="images/02_1st_dev-2025-10-12-16-43-46.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">

 こんなんわかるか。これ、普通に自分でやってたら絶対解決できなかったと思います。そのあと、サポートページで解除するための方法と申請文も出してくれて、さらにそのあとのやり取りも頼んで解決しました。
 <img src="images/02_1st_dev-2025-10-12-16-47-57.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">

 

##　テキストからの音声生成を実現する
 さて、APIの利用ができるように準備が整ったので、本筋の開発を続けます。目的は音声ファイルを生成するところまででした。
 具体的にどうやって音声化するかをまず相談します。
 <img src="images/02_1st_dev-2025-10-12-16-54-02.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">

 Google Cloud　TTS APIを使うことにします。すでにOpenAIのAPIを使うときにエラーを解決した経験があるのでここはわりとすいすいとエラーを解決できました。

 API連携はうまくいったものの、期待通りの音声ファイルができない問題が発生します。すでにナレーション台本を作る基本的な流れは考えていたものの、台本に余計な指示や記号が入ってしまってそれが取れない。TTSは忠実に「カッコ」とかまで読んでしまう。
ChatGPTのプロンプトの問題なので、プロンプトを試行錯誤し、さらに最終的には力業ではずす（Javascriptで）という解決をしました。
  
  
## UIもつけてみる。動いた！
 エラーが解決できたので、全体で動かしてみることにします。HTMLを出してもらってファイルに保存、さてブラウザからアクセス。
 <img src="image.png" alt="alt text" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">

 どうやらいっぱつで動いた模様
 
<img src="images/02_1st_dev-2025-10-12-17-18-52.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">

    
 まあまあ苦労したものの、結構すんなりと進みました。とにかくやるべきことをどんどん教えてくれるので、それに従って行けばうまくいくような気がしていました。なんつってもAPI使えるようになったしね！　夢が膨らみます。




  
