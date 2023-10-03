---
layout: manual
category: management
title: Jekyllでウェブページを作る
---
## はじめに

KIKSでは、GithubPagesのメンテナンス性向上のために**Jekyll**(ジキル)というツールを導入しています。
CSSやJavaScriptなどの知識を最小限でウェブページを書くことができます。
このページでは、最低限マニュアルを書く人に覚えておいてほしいことをお伝えします。

## カテゴリを作る

`kiksworks.github.io/_カテゴリ名`というフォルダを作成してください。アンダーバーをお忘れなく。そして、`_config.yml`のcollections:を以下を参考にして編集してください。education-boardとmanagementが登録されていると、以下のようになります。

```title:_config.yml
collections:
  education-board:
   output: true
  management:
    output: true
```

## 目次の作成&登録
作成したカテゴリのフォルダに`index.html`を作成してください。
そして、中身を他のカテゴリのindex.htmlを参考に書き換えてください。5行目くらいにある以下の文を変更してください。  
`{％ assign sorted_tags = site.カテゴリ名 | sort %} `  
(サイト作成の都合上、左の％が全角になっています。半角の%に直してください。)

## ページを作る

マークダウンファイル(.md)か、HTMLファイル(.html)を用意してください。何も気にせず、いつもどおりに書いてください
そして、ファイルの一番上に以下の行を記述してください。

```title:FrontMatter
--- 
layout: default  
title: sample  
---
```

これはFront Matterという、ページの基本設定を行うコードです。  
layoutは、ページで使うレイアウトを指定します。
`kiksworks.github.io/_layouts`フォルダに保存されています。  
titleはページのタイトルを指定します。

マニュアルを作っているなら以下のようにしてください。

```title:FrontMatter
--- 
layout: manual  
title: sample 
category: カテゴリ名 
---
```

これを先ほど作成したカテゴリのフォルダに入れてkiksworks.github.ioリポジトリにPushするだけで、Jekyllが勝手にページを作ってくれるはずです。

## もっと知りたい人
とりあえず、最低限これだけ知っていればマニュアル作成くらいはできると思います。  
サイトの管理などもっと高度なことがしたい人は、Jekyllを使っているPCに導入することで、PC上でビルドしてテストすることができます。詳しくは[Jekyllのページ](http://jekyllrb-ja.github.io/)を見てください。
