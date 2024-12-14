+++
title = "エスカレーション対応のチケット駆動開発 ふりかえり"
date = 2020-12-19T14:50:25+09:00
+++

[#ssmjp Advent Calendar 2020](https://adventar.org/calendars/5210) 19日目の記事です。

お話する時間は無かったので、
「チケット駆動開発がまわりはじめるまでの取り組み」では、
「誰が」「何をするか」「何をしているか」「どこまで出来ているか」が
少しずつチケットとして見えるようになってきたとだけ書きました。

「 [エスカレーション対応のチケット駆動開発 中編](/okr-tidd-case/escalation-tidd-part2) 」
「 [エスカレーション対応のチケット駆動開発 後編](/okr-tidd-case/escalation-tidd-part3) 」
を半年間掛けて行ってきた結果、
「 [エスカレーション対応のチケット駆動開発 前編](/okr-tidd-case/escalation-tidd-part1) 」
にて観測していたことがどのようになっていったか、得られた知見について書きました。

チケット駆動開発がまわりはじめるまでの取り組み

https://speakerdeck.com/zinrai/okr-tidd-case

## 効果

「 [エスカレーション対応のチケット駆動開発 前編](/okr-tidd-case/escalation-tidd-part1) 」
にて観測していた状況が、どのようになったかについて書いていきます。

### 窓口の全容を把握できた

窓口は全部で16あることがわかりました。
窓口の全容を知る人がいないなか、チームメンバーを少しずつ巻き込み、
ヒアリングしていったことで、チームにくる問い合わせ、
アラート対応などの窓口が、どれだけ存在しているかの全容を把握することができました。
これだけの窓口から問い合わせ、アラート対応を受けていたということを
この取り組みにより、チームで認識を合わせることができました。
窓口をチケットのカテゴリとして表現することで、
どの窓口からきた件であるかを観測できるようになっています。

### Slack DM はパブリックな場所に誘導する

Slack にチャンネルが沢山ある状況で、
どこに投げたらよいからからず、知ってそうな人に DM するという状況はあります。

だた Slack DM で個人に問い合わせがきて、そこに回答してしまうと、
他のメンバーは状況を観測できなくなってしまうため、
良い状況とは言えないという認識をチームで合わせました。

Slack DM で問い合わせが来た場合は、
問い合わせてきた相手に対して、
パブリックなチャンネルに誘導しましょうという形をとり、
他のメンバーが状況を観測できない状況を無くしていっています。

### 対応を宣言する

能動的に問い合わせ、アラートを取っていくというスタイルは一切変更していません。
だた、リアクション無しにそれを行ってしまったがために、
同じ件に2人が対応していたというような状況が発生していました。
これから自分が対応するという意思表示をしましょう、
実際にはこうしていきましょうということをチームで認識を合わせ行っています。
Slack の窓口では対応を宣言するためのリアクションをする、
メール の窓口では、 Slack に件名をコメントし対応を宣言するといった形をとっています。
同じ問い合わせ、アラートに複数名が対応していたというとは無くなりました。

### 対応状況がチケットにより見えるようになった

問い合せ、アラート対応はチケットとして起票されるようになり、
「誰が」「何に」対応しており、「どのような状況であるか」が見えるようになりました。
チームミーティングにて、問い合せ、アラート対応の状況が共有されたときに、
「あとでチケットにコメントしておきますね」といった、
対応しているメンバー以外もチケットをベースにコミュニケーションできるようになりました。

### 対応状況の確認が容易になった

今までは、「誰が」「何に」対応していて、
終わっているのか、終わっていないのか、
確認する術が無く全くわからない状態でした。

問い合せ、アラート対応の状況確認が、
チケットを一覧するだけでよくなり、
クローズとなっていないチケットも容易に集計できるようになり、
「この件、最後の更新から一週間経過しているけど何かあった？」
というようなコミュニケーションがとれるようになりました。

### ナレッジとして利用できた

問い合せ、アラート対応がチケットに起票され、
チケットクローズ時に対応した内容、
相手への回答をチケットにまとめるようになりました。
担当者以外が、
対応した内容を参照できるようになったことにより、
過去に対応したチケットを参照し、
他のメンバーが、問い合せ、アラートに対応できるような流れができていきました。

## 知見

進めていく中で得られた知見について書いていきます。

### 担当者を変わってもらう心理的ハードルの解消

初期メンバーで進めていたときに
「問い合せ、アラートを取ってみたが、
自分では解決に持っていくことが難しかったので、
別のメンバーに引き継ぎたいということがある。
だた担当者を変わってもらう心理的ハードルがある。」
というような声が上がりました。

チームミーティングの雰囲気から、
問い合せ、アラート対応の担当者が自身に変更となるような場合に
嫌悪感を示すような人は、チームメンバーはいなさそうな印象はありました。
だた、チームでの認識は合わせているわけではないので、
新卒メンバーがうまく立ち回ることができなさそうだということがわかりました。

チームミーティングにて、
担当者に割り当たる可能性があることをチームメンバーに共有し、
そうしてもらって全く問題ないという認識をチームで合わせました。

### 恒久対応を追い出す

アラート対応のチケットの中で、恒久対応まで行おうとし、
チケットのクローズが長期化してしまっているという状況を観測しました。
アラート対応は、復旧対応までとし、恒久対応は、
親子でチケットを管理しているプロジェクトにて進めていくという認識をチームで合わせ、
恒久対応をアラート対応の中から追い出すようにしました。

### 別 Redmine で管理している対象は除外する

別 Redmine でチケットが管理されており、
転記する形となっている対象があることが、
会議体でチームメンバーと話している中でわかりました。
対応状況が見えないことが課題となっているため、
別 Redmine でチケットが管理され、
対応状況が観測できている対象をわざわざ転記する必要はないというとで、
チケット起票する対象から除外しました。

### チケットの生存期間を観測できた

問い合せ、アラート対応にて起票されたチケットの作成日と終了日の差から、
チケットの生存期間を集計してみたところ、87パーセントのチケットは、
チケットが作成されてから7日以内にクローズされていることがわかりました。

この結果から、
ほとんどのチケットは数週間も掛かるような性質を持っていないということがわかったので、
チケットが起票されてから、7日以上経過しているチケットに対して Slack で担当者にメンションする
「 [チケット駆動開発の運用にて開発した小さなツール達](/posts/tidd-tools) 」
にて紹介した project-escala-activiety を開発しました。