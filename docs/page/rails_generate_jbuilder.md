---
layout: page
---

### 説明

jbuilderファイルを生成

### 使い方

    $ rails generate jbuilder 名前 [フィールド:型..] [オプション]

| オプション              | 説明                                   | デフォルト値 |
| ----------------------- | -------------------------------------- | ------------ |
| --skip-namespace        | namespaceの生成をスキップ              |              |
| --skip-collision-check  | コリジョンチェックをスキップ           |              |
| --force-plural          | 与えられたモデル名を強制的に使用       |              |
| --model-name=MODEL_NAME | 使用するモデル名                       |              |
| --timestamps            | timestampsファイルを生成するか         | true         |
| -f, --force             | ファイルが存在する場合に上書き         |              |
| -p, --pretend           | ドライラン                             |              |
| -q, --quiet             | 進捗情報を非表示                       |              |
| -s, --skip              | 既に存在するファイルはスキップ |              |
| -h, --help              | ヘルプ                                 |              |
| -v, --version           | バージョンを表示                       |              |

### 例

    $ rails generate jbuilder hoge
