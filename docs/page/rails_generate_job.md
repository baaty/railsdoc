---
layout: page
---

### 説明

app/jobs以下ににアクティブなジョブファイルを生成

### 使い方

    $ rails generate job 名前 [オプション]

### オプション

| オプション                | 説明                                   | デフォルト値 |
| ------------------------- | -------------------------------------- | ------------ |
| --skip-namespace          | namespaceの生成をスキップ              |              |
| --skip-collision-check    | コリジョンチェックをスキップ           |              |
| --queue=QUEUE             | 生成されたジョブのキューの名前         | default      |
| -t, --test-framework=NAME | 呼び出されるテストフレームワークを指定 | test_unit    |
| -f, --force               | ファイルが存在する場合に上書き         |              |
| -p, --pretend             | ドライラン                             |              |
| -q, --quiet               | 進捗情報を非表示                       |              |
| -s, --skip                | 既に存在するファイルはスキップ |              |
| -h, --help                | ヘルプ                                 |              |
| -v, --version             | バージョンを表示                       |              |

### 例

    $ rails generate job hoge
