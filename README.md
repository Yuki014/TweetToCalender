# TweetToCalender
リツイートしたツイートを自動でGoogleカレンダーに入れるアプリ  
実装方法はある程度知識があったり自力で調べられる人向けです  
もし、使いたいという声が多ければ追記します(多分)  

# 実装方法
1. ツイッターAPIを取得する  (Developerアカウントの申請方法は[こちらを参考](https://qiita.com/kngsym2018/items/2524d21455aac111cdee))  
1.CallBack URLを必ず2つ以上設定する必要があるので、それぞれ以下のようにする  
   - `https://script.google.com/macros/d/自分のスプレッドシートのシートID/usercallback`  
   - `https://script.google.com/macros/d/自分のスプレッドシートのシートID/user/callback`  
1. GoogleDriveにスプレッドシートを新規作成する
1. トップバーの ツール > スクリプトエディタ からスクリプトエディタを開く
1. このリポジトリにある main > gettimeline の中身をコピペする
1. 以下の部分をそれぞれ自分のものに書き換える  
1.1行目のCONSUMER_KEY  
2.2行目のCONSUMER_SECRET  
3.59行目のopenByIdのID  
4.60行目のgetSheetByNameのシート名  
5.82行目のGmailアドレス
1. トップバーの リソース > ライブラリ をクリック
1. ライブラリを追加に以下のIDを入力 `1CXDCY5sqT9ph64fFwSzVtXnbjpSfWdRymafDrtIZ7Z_hwysTY7IIhi7s`  
1.上記のライブラリのバージョン12を選択し、デベロッパーモードをONにする[こちらを参考](https://qiita.com/Ikanogo/items/1dce33c26559eac56a03)
1. 「関数を選択」からgetAuthorizeURLを選択して実行
1. 初回起動時は(おそらく)「Googleアカウントにこのスクリプトの実行を許可しますか？」的なウィンドウが出てくるので「許可」する
1. もう一度実行すると今度はよくあるツイッターアプリ連携の認証画面が出てくるので、認証する
1. スクリプトエディタの時計みたいなアイコンをクリックし、トリガー設定ページを開く
1. トリガーを追加をクリックし、実行する関数を選択のところを「getTimeLine」にする
1. イベントのソースを選択のところを「時間主導型」にする
1. 「時間ベースのトリガーのタイプを選択」と「時間の間隔を選択」は好きな間隔を選ぶ(1分ごとでも1時間ごとでも好きなように)

# バグ報告や要望などの連絡先
G-mail:l.0.Yu.U.Ki.0.l@gmail.com  
Twitter:https://twitter.com/yuuki_25_25

# 免責事項
当サービスを利用したことによって生じた損害等の一切の責任を負いかねますので、ご了承ください。  
2019年5月22日　策定

2019年5月22日　改訂
