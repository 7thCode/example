### 環境構築手順
---
#### MacOS
---
##### xcode
まず、なにかと使用するAppleの標準開発環境"xcode"をインストール。
```bash
$ xcode-select --install
```
---
##### Node.js
Node.JSのインストールは２段階。
まずNode.JSのバージョン管理ツール"Nodebrew"をインストール。
その後Nodebrewで本体をインストール。
(Node.JSはバージョンアップが激しいため、バージョンアップを簡単に行えるよう。)
[nodebrew](https://github.com/hokaccha/nodebrew)
名前が似てるけど"Homebrew"とは一切関係がない。
---
###### Nodebrewのインストール
```
$ curl -L git.io/nodebrew | perl - setup
```
終了後にターミナルに表示されるPATHを.bashrcに追加し保存。
（以下、MacOS10.15以降では".bashrc"を".zshrc"と読み替えてください。)
```bash
$ nano .bashrc

export PATH=$HOME/.nodebrew/current/bin:$PATH
```
適用
```bash
$ source .bashrc
```
---
###### Node.JSのインストール
インストールできるNode.jsの最新バージョンを確認 
```bash
$ nodebrew ls-remote
```

Node.jsをインストール
```bash
$ nodebrew install-binary v12.16.0
```

*奇数バージョンは開発テスト用のため、常に偶数バージョンをインストールすること 
---
##### homebrew

次にMac用の各種ソフトウェアをインストールできるパッケージマネージャ"Homebrew"をインストール。
[Homebrew公式](https://brew.sh/index_ja)

```bash
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
$ brew doctor
Your system is ready to brew.
```
---
##### MongoDB

homebrew経由でMongoDBをインストール
```bash
$ brew tap mongodb/brew
$ brew install mongodb-community
```
