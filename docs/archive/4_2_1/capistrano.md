---
layout: page
---
### 説明
コマンドの実行を自動化

### 前提条件
* アプリケーションがバージョン管理ツールで管理されている
* デプロイ先のサーバにSSHでログインできる
* デプロイ先サーバのログインユーザが、インストールディレクトリを読み書きできる権限がある
* デプロイ先サーバにバージョン管理クライアントがインストールされている

### 簡単な流れ
1.  開発環境にRailsアプリを作成
2.  Railsアプリをcapistranoに対応
3.  config/deploy.rbを編集
4.  rake deploy

### インストール
    $ gem install capistrano

### 設定ファイルを生成
    $ capify アプリケーションのルートディレクトリ

### 例
    $ cd path/to/application
    $ capify .
    [add] writing '.Capfile'
    [add] writing './config/deploy.rb'
    [done] capified!

### デプロイの設定
#### 基本的な設定

設定項目         | 説明
------------ | -------------------------------
:application | アプリケーション名を設定
:repository  | アプリケーションを管理している構成管理ツールのレポジトリを設定
:deploy_to   | アプリケーションのデプロイ先のパスを指定
:use_sudo    | 各種操作でsudoするかどうかを指定
:runner      | サーバ上でsudoして各種操作を実行するユーザ名を指定
:scm         | 構成管理ツールを指定
:deploy_via  | デプロイ方法を指定
:revision    | デプロイするリビジョンを指定

### 配布先のサーバにディレクトリツリーを作成
#### アクセス件の変更
    $ sudo visudo
    #Defaulrs requiretty <- コメントアウト

#### ディレクトリ作成
    $ cap deploy:setup

### デプロイを実行
    $ cap deploy

### 本番用のＤＢを作成
    $ cap deploy:migrate

### プロセスを起動
    $ cap script:start

### ロールバック
    $ cap deploy:rollback

### コミットするときに無視
* database.yml
* schema.rb
* log
* tmp