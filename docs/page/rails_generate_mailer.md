---
layout: page
---

### 説明

新しいメーラーとそのビューを生成

### 使い方

    $ rails generate mailer 名前 [メソッド..] [オプション]

| オプション                 | 説明                                   | デフォルト値 |
| -------------------------- | -------------------------------------- | ------------ |
| --skip-namespace           | namespaceの生成をスキップ              |              |
| --skip-collision-check     | コリジョンチェックをスキップ           |              |
| -t, --test-framework=NAME  | 呼び出されるテストフレームワークを指定 | test_unit    |
| -e, --template-engine=NAME | 呼び出されるテンプレートエンジンを指定 | erb          |
| -t, --test-framework=NAME  | 呼び出されるテストフレームワークを指定 | test_unit    |
| -f, --force                | ファイルが存在する場合に上書き         |              |
| -p, --pretend              | ドライラン                             |              |
| -q, --quiet                | 進捗情報を非表示                       |              |
| -s, --skip                 | 既に存在するファイルはスキップ |              |
| -h, --help                 | ヘルプ                                 |              |
| -v, --version              | バージョンを表示                       |              |

### 例

    $ rails generate mailer Notifications signup forgot_password invoice
