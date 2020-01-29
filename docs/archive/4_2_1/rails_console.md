---
layout: page
---
### 説明
コンソールを起動

### 使い方
    $ rails console [環境(test/development/production)] [オプション]

### オプション

オプション        | 説明
------------ | -----------------------
-s, -sandbox | 終了時にデータベースに関する変更をロールバック
-debugger    | デバックモードで起動
-irb         | irb
-h, --help   | ヘルプ

### 例
#### コンソール起動
    $ rails console
    Loading development environment (Rails x.x.x)
    irb(main):001:0>

#### 短縮実行
    $ rails c

#### production環境でコンソール起動
    $ rails console production
    Loading production environment (Rails x.x.x)
    irb(main):001:0>

#### コンソールでSQLの出力を表示
    $ rails console
    irb(main):001:0> ActiveRecord::Base.logger = Logger.new(STDOUT)