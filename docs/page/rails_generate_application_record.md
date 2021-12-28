---
layout: page
---

### 説明

application_recordファイルを生成

### 使い方

    $ rails generate application_record [オプション]

| オプション             | 説明                                   | デフォルト値  |
| ---------------------- | -------------------------------------- | ------------- |
| --skip-namespace       | namespaceの生成をスキップ              |               |
| --skip-collision-check | コリジョンチェックをスキップ           |               |
| -o, --orm=NAME         | 呼び出されるORMを指定                  | active_record |
| -f, --force            | ファイルが存在する場合に上書き         |               |
| -p, --pretend          | ドライラン                             |               |
| -q, --quiet            | 進捗情報を非表示                       |               |
| -s, --skip             | 既に存在するファイルはスキップ |               |
| -h, --help             | ヘルプ                                 |               |
| -v, --version          | バージョンを表示                       |               |

### 例

    $ rails generate application_record
