---
title: TwitterのWebページをサイドバーで使うためのまとめ
author: azu
layout: post
permalink: /2009/1125/res1488/
aktt_notify_twitter:
  - no
SBM_count:
  - '00014<>1355438309<>9<>0<>1<>4<>0'
dsq_thread_id:
  - 300802483
categories:
  - Firefox
tags:
  - css
  - Greasemonkey
  - twitter
  - web
---
**Twitterのウェブサイトをクライアントとして使うのに役立つGreasemonkeyとCSS | Web scratch**
:   [https://efcl.info/2009/0317/res613/][1]

以前書いたような記事と似たような記事を書きましたが、今回はシンプルにサイドバーでTwitterのWebページを表示する方法です。  
Greasemonkeyがサイドバーでも動作するようになったので、かなり快適になり、またWebページを表示するだけなので**APIを使わない**のが特徴です。

<br class="spacer_" /><figure id="attachment_1490" style="width: 121px;" class="wp-caption alignnone">

[<img class="size-medium wp-image-1490" title="ss-2009-11-25-22-40-16" src="https://efcl.info/wp-content/uploads/2009/11/ss-2009-11-25-22-40-16-121x300.png" alt="最終的な似た目" width="121" height="300" />][2]<figcaption class="wp-caption-text">最終的な似た目</figcaption></figure> 
<br class="spacer_" />

まずはCSSでサイドバーに合わせた形にする必要があります。

**nukumori wiki &#8211; Firefoxのサイドバーでtwitter.comするCSS**
:   [http://nukumori.org/hiki/?TwitterSidebarCSS][3]

にあるCSSを使ってサイドバーに合わせたものにしていきます。  
使い方は書いてあるのでそれをよく読んでCSSを反映させます。  
(ブックマークするのは<http://twitter.com/?sidebar> という適当なクリエを付けたURLです。  
[http://twitter.com/][4]だと通常見るときと混ざってしまうため。)

ブックマークではなく[Custom Buttons][5]を使ってtwitterをサイドバーに表示するボタンを作成する方法もあります。  
Twitterをサイドバーに表示するボタンを作成しておきました。

*   [<img style="margin: 0 6px;" src="data:image/png;base64,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" border="0" alt="Twitter sidebar" />Twitter sidebar][6]

*   [userChrome.css][7]  
    少し自分向けに修正したCSS(通常のTwitterページ向けも混ざってる)

次により使い易くするためのGreasemonkeyを入れていく。

*   <div>
      <div>
        <span><a href="http://gist.github.com/242700">Twitter Enhancements: Press Ctrl + Enter to Send Update.user.js</a></span>
      </div>
      
      <div>
        <div id="gist-embed" style="display: inline;">
          <input style="display: none;" size="25" src="%22http://gist.github.com/242700.js?file=Twitter+Enhancements%3A+Press+Ctrl+%2B+Enter+to+Send+Update.user.js%22%3E%3C/script%3E" type=" mce_src=" value="<script src=" />
        </div>
      </div>
    </div>

Ctrl+Enterでポストする。

*   [Twitter Change Style.user.js][8]

自分の投稿や、特定のワードが入ってる投稿を色分けする  
<cite></cite>[tyoro.exe: 投稿内容からマッチングしてスタイル変えるグリモン書いたよ！][9]

*   [TwitterAutoReloader.user.js][10]

自動更新の差分を自動で取得  
[Twitter webの自動差分更新Greasemonkeyスクリプトを書いてみた « H.LOG][11]

<br class="spacer_" />

自分は入れてませんが基本的にはTwitterのWebページと同じなので、

*   [PBTweet+][12]
*   [troynt&#8217;s Twitter Script][13]

など入れるのもありかもしれない。

<br class="spacer_" />

 [1]: https://efcl.info/2009/0317/res613/ "Twitterのウェブサイトをクライアントとして使うのに役立つGreasemonkeyとCSS | Web scratch"
 [2]: https://efcl.info/wp-content/uploads/2009/11/ss-2009-11-25-22-40-16.png
 [3]: http://nukumori.org/hiki/?TwitterSidebarCSS "nukumori wiki - Firefoxのサイドバーでtwitter.comするCSS"
 [4]: http://twitter.com/?sidebar
 [5]: https://addons.mozilla.org/ja/firefox/addon/2707
 [6]: custombutton://%3C%3Fxml%20version%3D%221.0%22%20encoding%3D%22UTF-8%22%3F%3E%0A%3Ccustombutton%20xmlns%3Acb%3D%22http%3A//custombuttons2.com/%22%3E%0A%20%20%3CCb2Ver%3E3.1.0%3C/Cb2Ver%3E%0A%20%20%3Cname%3ETwitter%20sidebar%3C/name%3E%0A%20%20%3Cimage%3E%3C%21%5BCDATA%5Bdata%3Aimage/png%3Bbase64%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%3D%5D%5D%3E%3C/image%3E%0A%20%20%3Cmode%3E0%3C/mode%3E%0A%20%20%3Ccode%3E%3C%21%5BCDATA%5Bvar%20title%20%3D%20%22Twitter%22%3B%0Avar%20uri%20%3D%20%22http%3A//twitter.com/%3Fsidebar%22%3B%0Avar%20sidebarTitle%20%3D%20document.getElementById%28%22sidebar-title%22%29.value%3B%0Avar%20sidebarBox%20%3D%20document.getElementById%28%22sidebar-box%22%29%3B%0Aif%20%28title%20%3D%3D%20sidebarTitle%29%20%7B%0A%09toggleSidebar%28%29%3B%0A%7D%20else%20%7B%0A%09openWebPanel%28title%2C%20uri%29%3B%20%20%0A%7D%5D%5D%3E%3C/code%3E%0A%20%20%3Cinitcode%3E%3C%21%5BCDATA%5B/*Initialization%20Code*/%5D%5D%3E%3C/initcode%3E%0A%20%20%3Caccelkey%3E%3C%21%5BCDATA%5B%5D%5D%3E%3C/accelkey%3E%0A%20%20%3Chelp%3E%3C%21%5BCDATA%5B%5D%5D%3E%3C/help%3E%0A%3C/custombutton%3E "Twitter sidebar"
 [7]: http://gist.github.com/242683
 [8]: http://gist.github.com/242666
 [9]: ../2009/0317/res613/%5C
 [10]: http://gist.github.com/242701
 [11]: http://hazisarashi.com/2009/11/17/twitter-web%E3%81%AE%E8%87%AA%E5%8B%95%E5%B7%AE%E5%88%86%E6%9B%B4%E6%96%B0greasemonkey%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%97%E3%83%88%E3%82%92%E6%9B%B8%E3%81%84%E3%81%A6%E3%81%BF%E3%81%9F/
 [12]: http://twitter.trauma2u.com/pbtweet/
 [13]: http://userscripts.org/scripts/show/40617
