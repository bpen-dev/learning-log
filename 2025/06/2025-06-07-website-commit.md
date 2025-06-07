# yyyy-mm-dd

## 今日やったこと・学んだこと
今日のゴール　環境を整えて、最初の静的ページを GitHub にコミットする
- PowerShellでwslのインストール
- Microsoft StoreでUbuntu LTSのインストール
- ubuntuでユーザー設定
```sudo apt update && sudo apt upgrade -y```
と入力し、システム全体を最新状態に。
- Gitのインストール
```sudo apt install -y git curl build-essential ```
- Gitのユーザー情報の登録
```git config --global user.name "あなたの名前"
git config --global user.email you@example.com```
- SSH鍵の作成・登録
```ssh-keygen -t ed25519 -C "you@example.com"```
パスフレーズは空でも設定しても OK
- 接続テスト 
```ssh -T git@github.com```
- GitHub 上で新規リポジトリを作成
- ローカルにclone
```git clone git@github.com:あなたのユーザー名/リポジトリ名.git```
- VSコード起動
```code .``` 　
- index.html と style.css の作成
- GitHubにコミット
```git add . #ステージするファイルを指定　
git commit -m "初回：静的ページ骨組み作成" 　
git push origin main ```

## 疑問・課題
- 

## メモ
- wslとは、Windows Subsystem for Linux の略称で、Windows 上で Linux をネイティブに動かす仕組み。
- WSL バージョンは、WSL1／WSL2 のどちらかを指す。
　　・WSL1：Windows のカーネル呼び出しをエミュレートして動作
　　・WSL2：軽量な実際の Linux カーネルを Hyper-V ベースで動作
　通常は WSL2 のほうが高速で互換性が高い
- ubuntuとは、Linux ディストリビューション。LTS版とは、“Long Term Support” の略で、長期サポートがある。
- UNIXとは、969年に米ベル研究所で開発が始まったOSの一種
- mdファイルにおいて、‘（バッククオート）３個で挟むとコードブロックにできる。SHIFT + ＠で打てる。
- ed25519とは、公開鍵暗号アルゴリズムの一つで、楕円曲線（Edwards curve）を使う。
- パスフレーズは空でもいいの？
- SHA256:のあとが公開鍵。

## 次に起動するときは
```cd my-static-site/
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
code .```
