# gitの操作で分からなかった事をメモするmd


1. 初めてリポジトリ作成時に登録でrejecte発生

* 手順＆状況
  
github側に初めてリポジトリを作成

Git bushでリポジトリに挙げたいファイルの場所で
  ```
  git init
  ```
よってリポジトリ(ローカル)を作る

そして以下の手順を踏む

```
git add 追加するファイル

git commit -m "コメント"

git remote add origin 追加するリポジトリのURL
```

ここまでは問題なし。問題は次に発生

```
git push origin master
```
すると以下のエラーが表示

```
To https://github.com/c0117312/web-
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/c0117312/web-'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```

* 発生した原因

実はgithubのリポジトリを作成した時、README.mdも追加したが、これがローカル側に認識されていないので、rejectされた。

* 解決方法

流れは以下の通り。まずfetchする事でローカルにREADMEを追加する。

```
git fetch
```

更に**merge**する。その時に **--allow-unrelated-histories** のオプションを追加する。これは本来マージする時の共通の分岐元を持たないブランチをマージする。

```
git merge --allow-unrelated-histories origin/master
```

ここまで来たら後はいつもの

```
git push orgin master
```
この問題は終了




