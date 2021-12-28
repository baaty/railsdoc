---
layout: page
---

### 説明

テストの実行とデータベースのリセット

### 使い方

    $ rails test [オプション] [ファイルかディレクトリ..]

### オプション

| 名前               | 説明                                         |
| ------------------ | -------------------------------------------- |
| -h, --help         | ヘルプを表示                                 |
| --no-plugins       | ミニテストプラグインの自動読み込みをバイパス |
| -s, --seed SEED    | ランダムシードを設定                         |
| -v, --verbose      | 進行状況を表示                               |
| -n, --name PATTERN | 実行されるフィルター                         |
| --exclude PATTERN  | 除外されるフィルター                         |

### 例

#### ファイルを指定してテスト

    $ rails test test/models/article_test.rb

#### ディレクトリを指定してテスト

    $ rails test test/models

#### ファイルに行番号で単一テスト

    $ rails test test/models/user_test.rb:27

#### 複数指定

    $ rails test test/controllers test/integration/login_test.rb
