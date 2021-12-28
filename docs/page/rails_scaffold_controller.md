---
layout: page
---

### 説明

アプリケーションの基本的な機能の一覧(index)、詳細(show)、新規作成(new/create)、編集(edit/update)、削除(destroy)するために必要なコントローラやビューをまとめて生成  
scaffoldとの違いはモデルやアセットが作られないこと

### 使い方

    $ rails generate scaffold_controller 名前 [カラム名:型..] [オプション]

### オプション

| オプション                  | 説明                                     | デフォルト値  |
| --------------------------- | ---------------------------------------- | ------------- |
| --skip-namespace            | namespaceの生成をスキップ                |               |
| --skip-collision-check      | コリジョンチェックをスキップ             |               |
| --force-plural              | 指定されたモデル名を強制的に使用         |               |
| --model-name=MODEL_NAME     | 使用するモデル名                         |               |
| --helper                    | helperファイルを生成するか               | true          |
| -o, --orm=NAME              | 呼び出されるORMを指定                    | active_record |
| --api                       | APIを生成するタイミング                  |               |
| --skip-routes               | config/routes.rbへのルート追加をスキップ |               |
| -e, --template-engine=NAME  | 呼び出されるテンプレートエンジンを指定   | erb           |
| --resource-route            | リソースルートを生成するか               | true          |
| -t, --test-framework=NAME   | 呼び出されるテストフレームワークを指定   | test_unit     |
| --jbuilder                  | jbuilderファイルを生成するか             | true          |
| --system-tests=SYSTEM_TESTS | システムテストを指定                     | test_unit     |
| --timestamps                | timestampsファイルを生成するか           | true          |
| -f, --force                 | ファイルが存在する場合に上書き           |               |
| -p, --pretend               | ドライラン                               |               |
| -q, --quiet                 | 進捗情報を非表示                         |               |
| -s, --skip                  | 既に存在するファイルはスキップ   |               |
| -h, --help                  | ヘルプ                                   |               |
| -v, --version               | バージョンを表示                         |               |

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

| ファイル                                | 説明                         |
| --------------------------------------- | ---------------------------- |
| app/controllers/XXXs_controller.rb      | コントローラファイル         |
| app/views/XXXs/index.html.erb           | すべてのリストを表示         |
| app/views/XXXs/edit.html.erb            | 編集ファイル                 |
| app/views/XXXs/show.html.erb            | 詳細ページ                   |
| app/views/XXXs/new.html.erb             | 新規ページ                   |
| app/views/XXXs/\_form.html.erb          | フォーム用ページ             |
| app/helpers/XXXs_helper.rb              | ヘルパー                     |
| test/functional/XXXs_controller_test.rb | コントローラ用テストファイル |
| test/unit/XXX_test.rb                   | モデル用テストファイル       |
| test/fixtures/XXXs.yml                  | フィクスチャファイル         |
| test/unit/helpers/XXXs_helper_test.rb   | テスト用                     |

### 例

    $ rails generate scaffold_controller CreditCard
