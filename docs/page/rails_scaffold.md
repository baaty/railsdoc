---
layout: page
---

### 説明

アプリケーションの基本的な機能の一覧(index)、詳細(show)、新規作成(new/create)、編集(edit/update)、削除(destroy)するために必要なコントローラ、モデル、ビューをまとめて生成

### 使い方

    $ rails generate scaffold 名前 [カラム名:型[:index]..] [オプション]

### オプション

| オプション                          | 説明                                       | デフォルト値        |
| ----------------------------------- | ------------------------------------------ | ------------------- |
| --skip-namespace                    | namespaceの生成をスキップ                  |                     |
| --skip-collision-check              | コリジョンチェックをスキップ               |                     |
| --force-plural                      | 指定されたモデル名を強制的に使用           |                     |
| -o, --orm=NAME                      | 呼び出されるORMを指定                      | active_record       |
| --model-name=MODEL_NAME             | 使用するモデル名                           |                     |
| --resource-route                    | リソースルートを生成するか                 | true                |
| --api                               | APIを生成するタイミング                    |                     |
| -c, --scaffold-controller=NAME      | 呼び出されるScaffoldコントローラ           | scaffold_controller |
| --migration                         | migrationファイルを生成するか              | true                |
| --timestamps                        | timestampsファイルを生成するか             | true                |
| --parent=PARENT                     | 生成されたモデルの親クラスを指定           |                     |
| --indexes                           | belongs_toカラムにインデックスを付与するか | true                |
| --primary-key-type=PRIMARY_KEY_TYPE | 主キーのタイプ                             |                     |
| -db, --database=DATABASE            | データベースの種類                         | sqlite3             |
| -t, --test-framework=NAME           | 呼び出されるテストフレームワークを指定     | test_unit           |
| --fixture                           | フィクスチャファイルを生成するか           | true                |
| -r, --fixture-replacement=NAME      | 呼び出されるフィクスチャを指定             |                     |
| --system-tests=SYSTEM_TESTS         | システムテストを指定                       | test_unit           |
| --helper                            | helperファイルを生成するか                 | true                |
| --skip-routes                       | config/routes.rbへのルート追加をスキップ   |                     |
| -e, --template-engine=NAME          | 呼び出されるテンプレートエンジンを指定     | erb                 |
| --jbuilder                          | jbuilderファイルを生成するか               | true                |
| -f, --force                         | ファイルが存在する場合に上書き             |                     |
| -p, --pretend                       | ドライラン                                 |                     |
| -q, --quiet                         | 進捗情報を非表示                           |                     |
| -s, --skip                          | 既に存在するファイルはスキップ     |                     |
| -h, --help                          | ヘルプ                                     |                     |
| -v, --version                       | バージョンを表示                           |                     |

### カラムの型

| データ方  | 説明           |
| --------- | -------------- |
| string    | 文字列         |
| text      | 長い文字列     |
| integer   | 整数           |
| float     | 浮動小数       |
| decimal   | 精度の高い小数 |
| datetime  | 日時           |
| timestamp | より細かい日時 |
| time      | 時間           |
| date      | 日付           |
| binary    | バイナリデータ |
| boolean   | Boolean型      |

### 生成されるファイル

| ファイル                                  | 説明                     |
| ----------------------------------------- | ------------------------ |
| db/migrate/YYYYMMDDHHMMSS_create_xxxes.rb | マイグレーションファイル |
| app/models/xxx.rb                         | モデルファイル           |
| app/controllers/xxxes_controller.rb       | コントローラファイル     |
| app/views/XXXs/index.html.erb             | すべてのリストを表示     |
| app/views/XXXs/edit.html.erb              | 編集ファイル             |
| app/views/XXXs/show.html.erb              | 詳細ページ               |
| app/views/XXXs/new.html.erb               | 新規ページ               |
| app/views/XXXs/\_form.html.erb            | フォーム用ページ         |
| app/views/xxxes/\_xxx.html.erb            |                          |
| app/helpers/xxxes_helper.rb               | ヘルパー                 |
| test/models/xxx_test.rb                   | モデルテスト             |
| test/fixtures/xxxes.yml                   | フィクスチャテスト       |
| test/controllers/xxxes_controller_test.rb | コントローラテスト       |
| test/system/xxxes_test.rb                 | システムテスト           |
| app/views/xxxes/index.json.jbuilder       | Jbuilderファイル         |
| app/views/xxxes/show.json.jbuilder        | Jbuilderファイル         |
| app/views/xxxes/\_xxx.json.jbuilder       | Jbuilderファイル         |

### 例

#### 最小の引数

    $ rails generate scaffold post

#### 属性を指定

    $ rails generate scaffold post title:string body:text published:boolean
