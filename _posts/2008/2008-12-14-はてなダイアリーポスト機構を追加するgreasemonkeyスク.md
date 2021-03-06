---
title: はてなダイアリーへのポスト機構を追加するGreasemonkeyスクリプト
author: azu
layout: post
permalink: /2008/1214/res394/
SBM_count:
  - '00003<>1355344048<>1<>0<>1<>1<>0'
dsq_thread_id:
  - 302207643
categories:
  - Greasemonkey
tags:
  - blog
  - Greasemonkey
  - はてな
---
元ネタ

**Greasemonkeyに、はてブポスト機構を追加するGreasemonkeyスクリプト**
:   <http://d.hatena.ne.jp/nastack/20080610/1213100873>

はてなダイアリー版が有れば結構便利そうなので、作成してみた。  
単体では特に意味はないGreasemonkeyなので、他のGreasemonkeyから呼び出して使用します。  
@includeの初期値が*となってしますが、使うところに限定する方がいいかも。

*   <a href="http://gist.github.com/raw/35464/b477745514bfcdb8fc1f7c1a387883d9b34a0b7d?hateda_poster.user.js" target="_blank">hateda_poster.user.js</a>

[gist: 35464 — GitHub][1]

使い方ははてブ版とほとんど同じで、上のをインストールしてなるべく上の方におきます。  
Altキーを使って移動させる。  
[<img class="alignnone size-medium wp-image-395" title="screenshot1" src="https://efcl.info/wp-content/uploads/2008/12/screenshot1-300x261.png" alt="" width="300" height="261" />][2]

**ポスト機構の使い方**

<pre class="brush:javascript;">if(!window.Hateda)return; //ポスト機構ができていなかったら終了する

var atom = new window.Hateda(
	"userID", //ID
	"password" //パスワード
).include(this);
</pre>

IDとパスワードはどちらも文字データで入れてください。

<pre class="brush:javascript;">var userID = "userID"//ID
var passWD = "password" //パスワード
var atom = new window.Hateda(
	userID, //ID
	passWD //パスワード
).include(this);
</pre>

という感じでも大丈夫です。

上でユーザーの情報をポスト機構に割り当ててから、実際にポストさせます。

<pre class="brush:javascript;">atom.post(
		["test", "tags"], //タグ 配列データ
		"titlename",      //title
		"comment",    //コメント
		function (){ //ポストが完了時実行される
			console.log("post!")
		}
	)
</pre>

ポスト機構はかなり手抜きで日付は設定させてないので、常に最新の位置にポストしています。

 [1]: http://gist.github.com/35464
 [2]: https://efcl.info/wp-content/uploads/2008/12/screenshot1.png
