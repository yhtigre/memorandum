# README - playbooks

## 概要
WEBサーバを構築する。

## 準備
Backlog Gitリポジトリからローカル環境へチェックアウトする。
クローンでもよいが余分なファイルも取得してしまうため、ここではチェックアウトの手順について記述する。

1. 適当なディレクトリを作成
```Bash
$ mkdir XYZ_playbooks
```

2. Git初期化
```Bash
$ cd XYZ_playbooks
$ git init
```

3. スパースチェックアウト機能を有効化
```Bash
$ git config core.sparsecheckout true
```

4. リモートリポジトリ(Backlog)をローカルリポジトリに登録
```Bash
$ git remote add origin ...
```

5. Ansibleプレイブックを含んだディレクトリを記述
```Bash
$ echo "playbooks/" > .git/info/sparse-checkout
```

6. リモートリポジトリの内容をローカルリポジトリに反映
```Bash
git pull origin master
```

7. Ansibleプレイブックをチェックアウト
```Bash
$ git checkout
```

## 使い方
1. initプレイブックを実行する
```Bash
$ cd init
$ ansible-playbook init.yml 
```

2. tbo_serverプレイブックを実行する
```Bash
$ cd tbo_server
$ ansible-playbook server.yml 
```
