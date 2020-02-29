### 環境構築手順
---
#### MacOS
---
@snap[midpoint span-80]
##### xcode
###### まず、なにかと使用するAppleの標準開発環境"xcode"をインストール。
@box[bg-black text-white]($ xcode-select --install)
@snapend
---
@snap[midpoint span-80]
##### Node.js
Node.JSのインストールは２段階。
まずNode.JSのバージョン管理ツール"Nodebrew"をインストール。
その後Nodebrewで本体をインストール。
(Node.JSはバージョンアップが激しいため、バージョンアップを簡単に行えるよう。)
[nodebrew](https://github.com/hokaccha/nodebrew)
名前が似てるけど"Homebrew"とは一切関係がない。
@snapend
---
@snap[midpoint span-80]
###### Nodebrewのインストール
@box[bg-black text-white]($ curl -L git.io/nodebrew | perl - setup)
終了後にターミナルに表示されるPATHを.bashrcに追加し保存。
（以下、MacOS10.15以降では".bashrc"を".zshrc"と読み替えてください。)
@box[bg-black text-white]($ nano .bashrc)
@box[bg-black text-white](export PATH=$HOME/.nodebrew/current/bin:$PATH)
適用
@box[bg-black text-white]($ source .bashrc)
@snapend
---
@snap[midpoint span-80]
###### Node.JSのインストール
インストールできるNode.jsの最新バージョンを確認 
@box[bg-black text-white]($ nodebrew ls-remote)
Node.jsをインストール
@box[bg-black text-white]($ nodebrew install-binary v12.16.0)
*奇数バージョンは開発テスト用のため、常に偶数バージョンをインストールすること 
@snapend
---
@snap[midpoint span-80]
##### homebrew
次にMac用の各種ソフトウェアをインストールできるパッケージマネージャ"Homebrew"をインストール。
[Homebrew公式](https://brew.sh/index_ja)

@box[bg-black text-white]（$ brew doctor)
@box[bg-black text-white]（Your system is ready to brew.)

@snapend
---
@snap[midpoint span-80]
##### MongoDB
homebrew経由でMongoDBをインストール
@box[bg-black text-white]（$ brew tap mongodb/brew)
@box[bg-black text-white]（$ brew install mongodb-community)
@snapend
---
