---
layout: page
---

### 説明

新しいRakeタスクを生成

### 使い方

    $ rails generate task 名前 [アクション..] [オプション]

| オプション             | 説明                                   | デフォルト値 |
| ---------------------- | -------------------------------------- | ------------ |
| --skip-namespace       | namespaceの生成をスキップ              |              |
| --skip-collision-check | コリジョンチェックをスキップ           |              |
| -f, --force            | ファイルが存在する場合に上書き         |              |
| -p, --pretend          | ドライラン                             |              |
| -q, --quiet            | 進捗情報を非表示                       |              |
| -s, --skip             | 既に存在するファイルはスキップ |              |
| -h, --help             | ヘルプ                                 |              |
| -v, --version          | バージョンを表示                       |              |

### 例

    $ rails generate task feeds fetch erase add
