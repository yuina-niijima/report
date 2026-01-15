## gitについて

- gitとはファイルの管理システム。更新履歴を残しておける。
- リポジトリの作成方法

1 Finderにフォルダ作成。わかりやすければどこでもok。

2 vscodeでファイル→フォルダーを開くから1で作成したフォルダを選択。


- テキストの作成方法

1 アイコンクリックしてリポジトリの初期化

![alt text](image.png)
![alt text](image-1.png)

2 ファイルを新規作成

- コミット

1 +マークからステージに上げる。もしくはターミナルでaddコマンド。ステージにあげるあげないで更新するファイルしないファイルを選択可能

![alt text](image-2.png)

2 メッセージを入力してコミット。メッセージは必須。コマンド：git commit -m “[comment]”

・githubへのアップロード

home→Repositories→New→名前などを入力してCreate repository

initからの場合

echo "# tesu" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/yuina-niijima/tesu.git
git push -u origin main

vscode側で初期化している場合
git remote add origin https://github.com/yuina-niijima/tesu.git
git branch -M main
git push -u origin main

上記コードをvscodeターミナルで使用

- その後の更新のアップロード

1 git add . / git add ファイル名　でアップロードしたいファイルをステージに上げる。

2 git commit -m "message"でコミット。メッセージは必須。変更内容などを簡単に書く。

3 git push でgithubにアップロード


- コマンド(よく使うもの。随時追加。)

<u>ローカルにリポジトリを作成し、リモートにプッシュする</u>

git init

git add .

git commit -m "Initial commit"

git remote add origin https://github.com/XXXX/XXXXXX.git

git push -u origin master


<u>ファイルの登録（コミットするため）</u>

git add <ファイル名>


<u>ファイルの変更や追加をコミット</u>

git commit -m "コミットメッセージ"


<u>ローカルの変更を確認する</u>

git status


<u>commitの変更履歴を見る</u>

git log


<u>リモートにpush</U>

git push origin <ブランチ名>


- コラボレーション機能

repositries→共有したいフォルダ選択→setting→collaborations→add peapleからメアド入力で追加


**参考サイト**

サル先生のgit入門
https://backlog.com/ja/git-tutorial/intro/01/

gitコマンド
https://qiita.com/2m1tsu3/items/6d49374230afab251337



