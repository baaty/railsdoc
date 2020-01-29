---
layout: page
---
### 説明
RubyGemsの管理ツール

### コマンド一覧

コマンド           | 説明
-------------- | -----------------------------
bundle install | 依存ライブラリのインストール
bundle update  | 依存ライブラリのアップデート
bundle package | 依存ライブラリを「vender/cache」以下にまとめる
bundle check   | 依存ライブラリがインストールされているかチェック
bundle list    | インストールされているライブラリの一覧
bundle show    | gemファイルのソースのパスを表示
bundle init    | gemを初期化

### 例
#### 依存関係のあるライブラリをインストール
    $ bundle install

#### 依存関係のあるライブラリをアップデート
    $ bundle update