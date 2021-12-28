---
layout: page
---

### 説明

新しいシステムテストを生成

### 使い方

    $ rails generate system_test 名前 [オプション]

| オプション                  | 説明                                   | デフォルト値 |
| --------------------------- | -------------------------------------- | ------------ |
| --skip-namespace            | namespaceの生成をスキップ              |              |
| --skip-collision-check      | コリジョンチェックをスキップ           |              |
| --system-tests=SYSTEM_TESTS | システムテストを指定                   | test_unit    |
| -f, --force                 | ファイルが存在する場合に上書き         |              |
| -p, --pretend               | ドライラン                             |              |
| -q, --quiet                 | 進捗情報を非表示                       |              |
| -s, --skip                  | 既に存在するファイルはスキップ |              |
| -h, --help                  | ヘルプ                                 |              |
| -v, --version               | バージョンを表示                       |              |

### 例

    $ rails generate system_test GeneralStories
