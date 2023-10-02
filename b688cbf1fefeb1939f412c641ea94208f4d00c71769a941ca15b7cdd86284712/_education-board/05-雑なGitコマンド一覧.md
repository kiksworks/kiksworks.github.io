---
layout: manual
title: 05-雑なGitコマンド一覧
category: Education-Board
---
ファイルをGit管理する際に最低限知っておいた方がいいコマンドをまとめておきます。  
ちなみに、-(ハイフン)のあとになにか文字がついているコマンド(git commit -aなど)がありますが、ハイフンをつけることによりオプションを指定することができます。  
コマンドはtabキーを押すと補完されます。補完されない場合はもう一度押すと候補が表示されます。積極的に活用して時短してみてください。いつもは補完されるけど、何故かできないときはコマンドを打ち間違えてる可能性があります。  

* ファイルをGitに対応させる  

  ```
  git init
  ```

* GitHub(remote)から自分のパソコン(local)にデータをコピーする(clone)  

  ```
  git clone アドレス(https://github.com/ユーザー名/リポジトリ名.git)
  ```

* remoteをlocalに登録する  

  ```
  git remote add リモート名 アドレス
  ```

* localをremoteと同期させる(fetch)

  ```
  git fetch リモート名
  ```

* 新しいブランチを作る  

  ```
  git branch 新しいブランチ名
  ```

* ブランチを切り替える  

  ```
  git switch ブランチ名
  ```

* コミットしていないlocalの変更を取り消す

  ```
  git checkout .
  ```

* remoteの情報をlocalに引っ張ってくる(pull)

  ```
  git pull リモート名 ブランチ名
  ```

* すべてのファイルをgit管理に追加

  ```
  git add .
  ```

* 変更されたファイルをコミットする

  ```
  git commit -a
  ```

  このあとに、何かしらエディタが開くので、コミットメッセージを書く。

* コミットをリモートと同期させる(push)

  ```
  git push リモート名 ブランチ名
  ```

* Gitの情報(現在のブランチ、コミット状況等)を見る

  ```
  git status
  ```

* コミットログを見る

  ```
  git log
  ```

* リモートの登録を見る

  ```
  git remote -v
  ```
