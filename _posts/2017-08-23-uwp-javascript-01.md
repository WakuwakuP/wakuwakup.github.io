---
layout: post
title: UWPアプリケーションをjavascriptで
category: Development
thumb: UWP01.png
comments: true
tag:
 - UWP
 - WinJS
 - mastodon
 - imastdon.net
---

1か月ほど前に[**imastodon.net**](https://imastodon.net)に登録しました.

そこでたくさんの副業開発者の方を見てモチベーションが作れたので
今回はUWPでマストドンクライアントアプリを作り始めました.

そして開幕でハマりました.


# 先駆者の情報が全然ない!!!

それもそのはずWinJS(ユニバーサルアプリ)で開発を始めているのですから!!

まあC#はなんだかんだ使ってきていなかったので
今回もjavascriptでできるならそれでいいやとか適当に決めたのです.

とりあえず1日開発して苦しんだことを並べていきましょう

* やっとのことで見つけたサンプルコードが動かない
* Reactの勉強の同時進行は無理だった

かなり苦しみながら頑張ってデザインを作りましたが残念なことにbootstrapを使って妥協しました.

![design.png]({{ site.baseurl }}/img/2017/08/23/design.png)

というわけで今後も開発を続けていきます．

明日はとりあえずOAuth認証とPOSTくらいは実装したいですね.

ストリーム取得は初めてやるのでOAuth認証等がしっかり出来ていることを確認してからにしますww.
