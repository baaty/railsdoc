---
layout: archive_page
---
### 説明
コンソールを起動  
コマンドラインでRailsアプリケーションとやるとりが可能

### 使い方
    $ rails console [環境 オプション]

### 環境

環境        | 説明
------------|------
test        | テスト環境
development | 開発環境
production  | 本番環境

### オプション

| オプション        | 説明                          |
|--------------|-------------------------------|
| -s, -sandbox | 終了時にデータベースに関する変更をロールバック |
| -debugger    | デバックモードで起動                  |
| -irb         | irb                           |
| -h, --help   | ヘルプ                           |

### 例
#### コンソール起動
    $ rails console
    Loading development environment (Rails x.x.x)
    irb(main):001:0>

#### production環境でコンソール起動
    $ rails console production
    Loading production environment (Rails x.x.x)
    irb(main):001:0>

#### コンソールでSQLの出力を表示
    $ rails console
    irb(main):001:0> ActiveRecord::Base.logger = Logger.new(STDOUT)

#### コンソール実行中にルーティングを取得
    >> app.root_path
    # "/"

#### コンソール実行中にヘルパーを取得
    >> helper.hoge

#### データを変更することなく実行
    $ rails console --sandbox