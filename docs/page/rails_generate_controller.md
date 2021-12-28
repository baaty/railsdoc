---
layout: page
---

### 説明

コントローラとビューを生成

### 使い方

    $ rails generate controller 名前 [アクション名..] [オプション]

### オプション

| オプション                 | 説明                                     | デフォルト値 |
| -------------------------- | ---------------------------------------- | ------------ |
| --skip-namespace           | namespaceの生成をスキップ                |              |
| --skip-collision-check     | コリジョンチェックをスキップ             |              |
| --skip-routes              | config/routes.rbへのルート追加をスキップ |              |
| --helper                   | helperファイルを生成するか               | true         |
| -e, --template-engine=NAME | 呼び出されるテンプレートエンジンを指定   | erb          |
| -t, --test-framework=NAME  | 呼び出されるテストフレームワークを指定   | test_unit    |
| -f, --force                | ファイルが存在する場合に上書き           |              |
| -p, --pretend              | ドライラン                               |              |
| -q, --quiet                | 進捗情報を非表示                         |              |
| -s, --skip                 | 既に存在するファイルはスキップ   |              |
| -h, --help                 | ヘルプ                                   |              |
| -v, --version              | バージョンを表示                         |              |

### 例

#### コントローラとビューを生成

    $ rails generate controller Page

#### アクションとビューも生成

    $ rails generate controller page title

#### 階層化されたコントローラを生成

    $ rails generate controller 'admin/page'
