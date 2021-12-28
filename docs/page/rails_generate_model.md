---
layout: page
---

### 説明

モデルを生成

### 使い方

    $ rails generate model 名前 [カラム名:型[:index]..] [オプション]

### オプション

| オプション                          | 説明                                       | デフォルト値  |
| ----------------------------------- | ------------------------------------------ | ------------- |
| --skip-namespace                    | namespaceの生成をスキップ                  |               |
| --skip-collision-check              | コリジョンチェックをスキップ               |               |
| --force-plural                      | 指定されたモデル名を強制的に使用           |               |
| -o, --orm=NAME                      | 呼び出されるORMを指定                      | active_record |
| --migration                         | migrationファイルを生成するか              | true          |
| --timestamps                        | timestampsファイルを生成するか             | true          |
| --parent=PARENT                     | 生成されたモデルの親クラスを指定           |               |
| --indexes                           | belongs_toカラムにインデックスを付与するか | true          |
| --primary-key-type=PRIMARY_KEY_TYPE | 主キーのタイプ                             |               |
| -t, --test-framework=NAME           | 呼び出されるテストフレームワークを指定     | test_unit     |
| --fixture                           | フィクスチャファイルを生成するか           | true          |
| -r, --fixture-replacement=NAME      | 呼び出されるフィクスチャを指定             |               |
| -f, --force                         | ファイルが存在する場合に上書き             |               |
| -p, --pretend                       | ドライラン                                 |               |
| -q, --quiet                         | 進捗情報を非表示                           |               |
| -s, --skip                          | 既に存在するファイルはスキップ     |               |
| -h, --help                          | ヘルプ                                     |               |
| -v, --version                       | バージョンを表示                           |               |

### カラムの型

| 型          | 説明           |
| ----------- | -------------- |
| string      | 文字列         |
| text        | 長い文字列     |
| integer     | 整数           |
| float       | 浮動小数       |
| decimal     | 精度の高い小数 |
| datetime    | 日時           |
| timestamp   | より細かい日時 |
| time        | 時間           |
| date        | 日付           |
| binary      | バイナリデータ |
| boolean     | Boolean型      |
| primary_key | プライマリキー |

### indexの種類

| 名前  | 説明         |
| ----- | ------------ |
| uniq  | ユニーク     |
| index | インデックス |

### 補足

- integer, string, text, binaryでは制限値を{ }で記述

### 例

#### モデルを生成

    $ rails generate model user

#### 階層を指定

    $ rails generate model admin/account

#### stringの制限が30文字

    $ rails generate model user pseudo:string{30}

#### indexを付与

    $ rails generate model user pseudo:string:index

#### ユニークなindexを付与

    $ rails generate model user pseudo:string:uniq
