---
layout: page
---

### 説明

Rails環境で動かすバッチ処理

### 使い方

    $ rails runner 実行するコード [オプション]

#### 短縮形

    $ rails r 実行するコード [オプション]

### オプション

| オプション      | 説明                                  |
| ---------- | ----------------------------------- |
| -e         | 環境((test/development/production)を指定 |
| -h, --help | ヘルプ                                 |

### 例

#### Rails環境で動かすバッチ処理

    $ rails runner "Model.hoge_method"

#### Rubyファイルを実行

    $ rails runner path/to/filename.rb

#### 標準入力から読み込んだRubyスクリプトを実行

    $ rails runner -
