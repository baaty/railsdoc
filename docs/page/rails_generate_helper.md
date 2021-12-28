---
layout: page
---

### 説明

新しいヘルパーを生成

### 使い方

    $ rails generate helper 名前 [オプション]

### オプション

| オプション                | 説明                                   | デフォルト値 |
| ------------------------- | -------------------------------------- | ------------ |
| --skip-namespace          | namespaceの生成をスキップ              |              |
| --skip-collision-check    | コリジョンチェックをスキップ           |              |
| -t, --test-framework=NAME | 呼び出されるテストフレームワークを指定 | test_unit    |
| -p, --pretend             | ドライラン                             |              |
| -f, --force               | ファイルが存在する場合に上書き         |              |
| -s, --skip                | 既に存在するファイルはスキップ |              |
| -q, --quiet               | 進捗状況を表示しない                   |              |
| -h, --help                | ヘルプを表示                           |              |

### 例

#### 新しいヘルパーを生成

    $ rails generate helper CreditCard

#### under_scoredの名前

    $ rails generate helper credit_card
