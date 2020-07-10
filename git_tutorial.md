# gitについて
youtubeで”互联网人都该懂点Git"の02課により学習資料を作成される。
## 2.1 基本操作
1. gitをインストールする。 
2. Windowsの場合Gitコマンド付属のGit Bashを開きます。

3. コマンドライン環境でgit --versionと入力し、Gitのバージョンが表示されることを確認します。
```git
$ git --version
```
4. Git上で使いたい情報を入力します。下記のコマンドで【ユーザー名】と【メールアドレス】の部分を、自分の情報に置き換えてください。

```
$ git config --global user.name "【ユーザー名】"
$ git config --global user.email 【メールアドレス】
```
5. 以下のコマンドで設定を確認できます。
```
$ git config --list
user.name=【ユーザー名】
user.email=【メールアドレス】
```
或、~/.gitconfigファイルに確認することができる。

```
cat ~/.gitconfig
```
6. cdで使用しているフォルダに移動してgitを構築する。
＃フォルダ内のファイルを確認
```
$ ll
```
7. レパートリーを構築
```
＄ git init
```
8. 状況確認
```
$ git status
```
9. レパートリーに追加する。
```
$ git add readme.md
```
⇒フォルダ内のファイルを全部でレパートリーに追加する
```
$ git add -A
```
⇒レパートリーを追加することができる。
```
$ git rm --cached <ファイル名>...
```
10. 最終に保存することを確定する

git commit -m "add ;;;"

***************************
***************************
## 2.2 githubの基本そおさ


1. gitbub のrepositoryに追加する.githubのwebでこの操作のtipsがある。

```
$ git remote add origin https://github.com/ciciwell/GIT_tuto.git
```
  > 注意：デフオイル、repositoryの名前はorign(変更可能).

2. repositoryを表示
```
$ git remote -v 
```
3. 最終に保存する
```
$ git push -u origin master
```
>+ originは repositoryの名前 
>+ masterは　repositoryの名前 
>+ -uを使用すると、これから、repositoryの名前とrepositoryの名前を入力しなくでも大丈夫である。

4. gitのrepositoryをdownloadする
$ git clone "https://help.github." <フォルダ名>

・ssh-keygenコマンドで鍵を生成する
https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

・githubに追加
$ git remote add origin https://github.com/tyoucc/firstgit.git

・githubに追加成功かどうか確認
$ git remote -v

・githubに保存する　（git push webの名前　brathの名前　-u でこの後直接にgit push を使用できる）
$ git push origin master -u


#参考資料
#youtubeの上で以下の映像を検索して、勉強する
GitHub简单使用教程
互联网人都该懂点Git

＃https://employment.en-japan.com/engineerhub/entry/2017/01/31/110000
