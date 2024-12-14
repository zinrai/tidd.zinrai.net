---
title: "チケット駆動開発に対する自身の考え 前編"
date: 2020-12-06T12:08:29+09:00
---

[#ssmjp Advent Calendar 2020](https://adventar.org/calendars/5210) 6日目の記事です。

自分なりに6年間ほど「チケット駆動開発」してきて、
現在どのような考えを持つに至っているかについて書いていたら結構なボリュームになったので、
前後編に分割しました。今回は、分割した半分のお話を書いています。

チケット駆動開発がまわりはじめるまでの取り組み

https://speakerdeck.com/zinrai/okr-tidd-case

## 未来の自分のために記録する

前職で、退職が決まり引き継ぎのために必要なドキュメンテーションとしてどのようなものがあるかを上司と洗い出していたときに、
上司から「認証基盤を運用するためのコマンドラインツールをどう使えばよいかをドキュメント化してもらいたい」と言われ、
開発者は退職しおり、私は使った記憶がなかったので「ちょっと私だとドキュメンテーションできない部分があるかもしれませんが、できるだけやってみます」と答えドキュメンテーションを進めました。

認証基盤をリプレイスしていた頃のチケットを漁れば当時の開発者の記録が出てくるだろうと思い漁っていたら、
自分自身が認証基盤を運用するためのコマンドラインツールをガッツリ使い作業している記録の残ったチケットが出てきました。
自分の記憶は信用できないなと再認識した瞬間であったとともに、
過去の自分は他人であることを知り、その他人の記録によって助けられました。
上司には「すいません。私、嘘を吐きました。過去の自分がしっかりツールを使っており、過去の自分の記録からドキュメンテーションできそうです。」と伝えました。

記憶というのは自分の都合のよいように書き換えられるため、
未来の自分を助けるのだというモチーベションでチケットへの記録を行うようにしています。

## 結果、誰かのための情報になる

前職では、人員不足を理由により若い独身の社員が借り出され、
二年半ほど自身の業務に加えて 24/365 のシフトの業務も兼務していました。
シフト中に監視システムから見掛けないアラートが発報されたときに
私の耳に入らないところで、どうやらサービスが終了していたということを Redmine のチケットを検索し見つけ出したというとが何度もありました。
私の耳には入りませんでしたが、チケットの記録として目に入る場所に情報があったので、
慌てることなく関係者に事実を確認し対応を進めることができました。

結果として誰かに情報を開示することになるということに繋がる体験もチケットへ記録するモチベーションの一つとなっています。

## 非同期に状況を把握できるよう情報をオープンにする

上司とのコミュニケーションが、「いま何をしているのか」から
「チケット番号 ○○ の件、ここまでの内容は読み取れたが、いまどんな状態か」
という形に変化していったとを書きました。

「いま何をしているのか」というようなコミュニケーションになってしまうと、
場合によっては、打ち合わせの機会を設けて同期的なコミュニケーションを取る必要が出てきます。

チケットにて自身のやっていること、考えていることなどを他の人にオープンにしたことで、
結果として、上司は非同期に私の状況を把握できるようになりました。

私がチケットにて情報をオープンにするようになってからは、
チームメンバーとのコミュニケーションも変わってきました。
私が考えていることや、これから進めようと考えていることに対して、
チームメンバーから「これこんな風にやってみたほうがよいかもしれないよ」と
フォローしてもらったことが数えきれないほどありました。

情報をオープンにすることで誰かに対して非同期に状況を伝えることができるという体験をしてからは、
私が「いつ」「何を」「どのように」「どのくらいの時間掛けて」やっているかということを
私に状況を聞かなくても誰でもチケットを集計すれば確認できるようにしています。

状況を聞かれた場合は、チケットを見せながら説明していくだけです。
信じられるのは自分の記憶ではなく、そこにある記録です。

情報をオープンにしなかったことで「いま何をやっているのか」
「何を考えているのか」わからないと指摘されたことはありますが、
情報がオープンになったことに対して何かを指摘されたことはありません。

## 覚えなくてよくなった

下記は、2020年11月に住んでいる賃貸物件で水漏れが発生し、
管理会社といろいろな対応をやりとりしたときに、
夫婦でのタスクを管理するために利用している Trello に作って進めたチケットになります。

* 水漏れ調査の立合い
* 水漏れの配管工事
* 水漏れ対応の事後処理
* 洗面所の壁紙の補修
* 洗濯機の凹みを管理会社に連絡
* 洗濯機のパネル修理

仕事や生活の中には様々な「決めごと」「やること」があり、
日々それらを片付けているなというのが、ここ数年ずっと思っていることです。
チケット駆動開発によって「決めごと」「やること」というのはチケットにして進めていくということを覚え、
「決めごと」「やること」というのは記憶に留めておく必要の無いものであるということを学びました。

「決めごと」「やること」をチケットとして管理するスペースを用意しておき、
全部チケットにしておけば忘れることができ、
「決めごと」「やること」を管理している場所だけ覚えておくというやり方は、
自身に記憶しておかなければならない情報量が圧倒的に少なくて、楽だなと思っています。

「決めごと」「やること」を記憶に頼ると
それが完了するまで休日だろうと休暇だろうと一生そのことに囚われ続けるし、
記憶に留めておくことにエネルギーを消費しなければならず疲れます。

チケット駆動開発をする以前の私は
「ハンターハンター」で「タブル」の念能力をヒソカに披露して敗北したカストロの状態だったなと感じています。
「容量(メモリー)のムダ使い」をして自ら苦しい状況に陥っていました。

「チケット駆動開発」によって「決めごと」「やること」をチケットにするようになったとにより、
それらを記憶に留めておくことから開放されました。
「決めごと」「やること」の記憶から開放された私は、思い出や習得したスキルの記憶に集中できるようになりました。

ISP の社員になって以降、年に2回ほど二週間以上の休暇をとるというとをしており、
休暇から戻ってきたときに「やることを思い出すのが大変ですよね」と言われたりします。
「決めごと」「やること」は「チケット駆動開発」によって外部に記録され、
戻ってきたときにどこを参照すればよいかということだけ覚えるようにしているため、
休暇から戻ったらそこから再開すればよいだけで、「思い出すのが大変」だと思ったことは一度もありません。
数週間の休暇だろうと、これから取得する数ヶ月の育休だろうと復帰してみせます。

「チケットを作るよりも、やったほうが早い」と言われることがよくあります。
私も、5分で出来ることが常に1つだけしかなく、
いますぐ実行できるのであればそうかもしれないなと考えます。
ただ、様々なやることを抱えていてかつ、
いますぐには実行できなかったりするというのがが現実ではないかと思います。
5分で出来ることが20個あって、それを記憶だけに頼り漏れなく全て実行していくというのは、
私の心の中のヒソカが「容量(メモリー)の無駄使い」と囁きます。
時間に関係無くチケット化することで、「容量(メモリー)の無駄使い」なく、
細切れに沢山ある「やること」を漏れなく実行できるようになりました。

* 記憶するのは自分の身になることや思い出
* 「決めごと」「やること」はチケット化し、 その事柄に囚われない、容量の無駄使いをしない
* 覚えるのは、どこで「決めごと」「やること」が管理されているかということだけ
* 私が「決めごと」「やること」を忘れたとしてもチケットが覚えているので問題なし

ということを考えながら日々、チケット駆動開発しています。