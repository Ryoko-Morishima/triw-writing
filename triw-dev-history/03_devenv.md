# 3.開発環境を整える（7月半ば）
## もっと自動化を進めたい
 ChatGPTに聞きながら進めたら、一部苦労はしたものの、無事ローカルで動くものができました。この勢いでアプリ作ったらいいんじゃない？と気持ちが一気に盛り上がります。音声ファイルを作るとか細かいこといってないでSpotifyと連携して音声ファイルはこっちにもっておいて、順番に読むとこもWeb上でやればいいじゃん！　できるできる！　
 というわけで、さて早速SpotifyAPIをまずは使えるようにしなくちゃな、と短絡的に考えます。
 すでにAPIやってるしできるだろ。ChatGPTに手順を聞きながら着々とすすめたら、知らない言葉がでてきた。
 「Redirect URI」の設定です。
 ChatGPT曰く。
 
 「Redirect URI（リダイレクトURI）には、「Spotify認証後にユーザーを戻すURL」を指定します。これは あなたのアプリ側で受け取るURL で、<b>環境によって変わります</b>。」「<b>開発中と本番環境</b>の両方を登録しておくのがオススメです。」
 
 本番環境！？　さらに。

 「必要であれば次は「OAuth認証を開始するURLを作る方法」や「Node.js/Next.jsでのトークン取得コード」も案内できます。<b>開発言語</b>や<b>環境</b>が決まっていれば教えてください！」

 いやーーーーーなんも決まってないよー。つーか考えたこともないよーーー。まあでもできたら公開したら楽しそうだしな、どうせならここで「開発環境」も整えていったほうがいいのかもしれないな……。
  
## 開発環境（Next.js）を入れるように勧められる
 ここまでは普通にテキストエディタでテキストファイルを作ってただけだったんですよね。私のやったことあるWebページって基本テキストファイルを作って、それをブラウザから読むっていうやつですから。一応知識としては最近のWeb開発は普通フレームワーク使うってことは知っています。でもいかんせん触ったことはない。いい機会だしやってみるのもいいかもね。わかんなくても聞けば答えてもらえるしね。

 まずNext.jsって何なのかを聞いてみます。
 <img src="images/03_devenv-2025-10-12-18-00-00.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">

 <img src="images/03_devenv-2025-10-12-18-00-45.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">

自信満々におすすめされたので、畳みかけて聞いてみます。

 <img src="images/03_devenv-2025-10-12-18-01-34.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">


 ここまで言われたらやるしかなくない？　しかしこの流れ、なんかマルチの勧誘めいてるよね。

## さらにVS Codeまで勧められる
 手順を聞きながらインストールを進めていきます。しかしインストールの過程でさらにVS Codeまで進められます。
 <img src="images/03_devenv-2025-10-12-18-07-35.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">

そして開発するならこれと言われて
<img src="images/03_devenv-2025-10-12-18-09-23.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">


 そしたら入れるしかないですよね。

　<img src="images/03_devenv-2025-10-12-18-09-52.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">


まあまあいろいろあったんですがスクショをChatGPTに貼り、解決しながらインストール完了です。

<img src="images/03_devenv-2025-10-12-18-12-00.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">

アクセスしたら……

 <img src="images/03_devenv-2025-10-12-18-12-20.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">

 でた。
 無理やり開発のスタートラインに立たされてしまった感がありありです。


## ついでにGIT HUB連携も
VS CODE だけでなく、開発やるならGIT HUBの連係まで勧められたのだった。
名前も知ってるしアカウントは持ってる。けど使いこなせてない。そりゃいままで開発ってものをしてないからね。
 一応説明も聞く。丁寧に教えてくれるものの覚えきれない。
 でも管理するにはよいものなのは知ってるので、とりあえず連携もしておく。やり方とかはとりあえずまかせてしまおう…。

## 準備でへとへと
next.jsで管理するファイルがHTMLとかじゃないので何が何だかわからない。しかもディレクトリが勝手にできていく（のか、ChatGPTの指定で作ったのかはちょっと忘れた）。
ディレクトリ構造がよくわからない。
さらに構成を整理する。

そんなこんなで開発に入るための準備にかなりの時間を要する。過去ログ見たらぐちってた。
<img src="images/03_devenv-2025-10-12-19-25-44.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">

ぐちると慰めてくれるのはこの段階ではかなり勇気づけられた。

## 開発プロジェクト名も決めた
 そんなわけで、ディレクトリ名とかつけないといけない都合上、もう仮でプロジェクト名もつけておく必要が出てきた。
 これもChatGPTと話ながら考えていったんですが、こういう相談はちょっと楽しい。はじめFM曲みたいに数字もいいかなーと思ったのだが、いまいちピンとこない。実際に周波数ってわけでもないし嘘っぽいしなー。
いろいろと考えて、なんか頭文字が取れそうなのがいいなと思って考え付いたのがこれ。
- The Radio I Wanted（略してTRIW）

今後、これをプロジェクト名として進めていきます。


## 開発するなら日誌も書いた方がいいよね
せっかく真面目にやることになったので、それなら開発日誌も書いておこうと思いました。なんで思ったのかは今となってはわかりません。真面目にやるなら記録しようと思ったのかもしれません。
 日誌ももちろんChatGPTに書いてもらいます。

<img src="images/03_devenv-2025-10-12-19-28-16.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">

<img src="images/03_devenv-2025-10-12-19-29-01.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">




  ログ見ると、いきなり開発モードに突入して不安になってたようです。頻繁に愚痴ったり心配と言ってて、そのたびに励まされてた。
<img src="images/03_devenv-2025-10-12-19-01-11.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">

<img src="images/03_devenv-2025-10-12-19-01-45.png" alt="" style="border:1px solid #e1e4e8;border-radius:6px;max-width:100%;height:auto;margin:8px 0 24px;">


いやー、改めて振り返ってみるとほんとにマルチっぽいな。でも応援されるとがんばれるのは確か。