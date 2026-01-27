# gitについて

- gitとはファイルの管理システム。更新履歴を残しておける。
- リポジトリの作成方法

1 Finderにフォルダ作成。わかりやすければどこでもok。

2 vscodeでファイル→フォルダーを開くから1で作成したフォルダを選択。


## テキストの作成方法

1 アイコンクリックしてリポジトリの初期化

![alt text](image.png)
![alt text](image-1.png)

2 ファイルを新規作成

## コミット

1 +マークからステージに上げる。もしくはターミナルでaddコマンド。ステージにあげるあげないで更新するファイルしないファイルを選択可能

![alt text](image-2.png)

2 メッセージを入力してコミット。メッセージは必須。コマンド：git commit -m “[comment]”

## githubへのアップロード

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

## ローカルにリポジトリを作成し、リモートにプッシュする

git init

git add .

git commit -m "Initial commit"

git remote add origin https://github.com/XXXX/XXXXXX.git

git push -u origin master


## ファイルの登録（コミットするため）

git add <ファイル名>


## ファイルの変更や追加をコミット

git commit -m "コミットメッセージ"


## ローカルの変更を確認する

git status


## commitの変更履歴を見る

git log


## リモートにpush

git push origin <ブランチ名>


## ラボレーション機能

repositries→共有したいフォルダ選択→setting→collaborations→add peapleからメアド入力で追加


## 直接mainにpushしてはいけない理由
- 壊れたコードが混入しやすい
- 誰が何をしたか追いにくく、prで履歴を可視化するため
- レビューが行われないため、品質が低下する

## Gitflowについて
- お天気アプリ作成においては、main及びfeature/spalashブランチを作成。適切なブランチを作成し派生を考える。

## お天気アプリのフロー
1. mainブランチ作成
2. 作業用のブランチ作成
3. 作業用ブランチをプッシュ
4. 作業用ブランチのプルリクエストを送る
5. マージする

## ブランチのプロテクト
- 直pushを防ぐ。下記サイトを参考にする。
- うまくプロテクトできないとき
- Enforcement statusはActiveになっているか？
- Branch targeting criteriaにmainブランチを追加しているか？
- [参考サイト](https://docs.github.com/ja/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/managing-a-branch-protection-rule)


## 参考サイト

サル先生のgit入門
https://backlog.com/ja/git-tutorial/intro/01/

gitコマンド
https://qiita.com/2m1tsu3/items/6d49374230afab251337


