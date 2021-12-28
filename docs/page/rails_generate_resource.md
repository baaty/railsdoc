---
layout: page
---

### 説明

RESTfulなリソース指向アプリケーションに適した空のモデルとコントローラを含む新しいリソースを生成

### 使い方

    $ rails generate resource 名前 [カラム名[:型][:index]..] [オプション]

| オプション                          | 説明                                       | デフォルト値 |
| ----------------------------------- | ------------------------------------------ | ------------ |
| --skip-namespace                    | namespaceの生成をスキップ                  |              |
| --skip-collision-check              | コリジョンチェックをスキップ               |              |
| --force-plural                      | 与えられたモデル名を強制的に使用           |              |
| --model-name=MODEL_NAME             | 使用するモデル名                           |              |
| -c, --resource-controller=NAME      | 使用するリソースコントローラ               | controller   |
| -a, --actions=ACTION ACTION         | リソースコントローラーのアクション         |              |
| --resource-route                    | リソースルートを生成するか                 | true         |
| --migration                         | migrationファイルを生成するか              | true         |
| --timestamps                        | timestampsファイルを生成するか             | true         |
| --parent=PARENT                     | 生成されたモデルの親クラスを指定           |              |
| --indexes                           | belongs_toカラムにインデックスを付与するか | true         |
| --primary-key-type=PRIMARY_KEY_TYPE | 主キーのタイプ                             |              |
| --db, --database=DATABASE           | 使用するデータベースを指定                 |
| -t, --test-framework=NAME           | 呼び出されるテストフレームワークを指定     | test_unit    |
| --fixture                           | フィクスチャファイルを生成するか           | true         |
| -r, --fixture-replacement=NAME      | 呼び出されるフィクスチャを指定             |              |
| --skip-routes                       | config/routes.rbへのルート追加をスキップ   |              |
| --helper                            | helperファイルを生成するか                 | true         |
| -e, --template-engine=NAME          | 呼び出されるテンプレートエンジンを指定     | erb          |
| -f, --force                         | ファイルが存在する場合に上書き             |              |
| -p, --pretend                       | ドライラン                                 |              |
| -q, --quiet                         | 進捗情報を非表示                           |              |
| -s, --skip                          | 既に存在するファイルはスキップ     |              |
| -h, --help                          | ヘルプ                                     |              |
| -v, --version                       | バージョンを表示                           |              |

### 例

#### 新しいリソースを生成

    $ rails generate resource post

#### カラム名あり

    $ rails generate resource post title:string body:text published:boolean
