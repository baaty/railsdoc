---
layout: page
---
### 説明
モデルを生成

### 使い方
    $ rails generate model 名前 [カラム名:型] [オプション]

### オプション

| オプション                          | 説明                   | デフォルト値       |
|--------------------------------|------------------------|---------------|
| --skip-namespace               | 名前空間をスキップする        |               |
| --old-style-hash               | 古いハッシュの形式を使う       |               |
| -o, -orm=名前                  | 使用するO/Rマッパー          | active_record |
| --migration                    | マイグレーションファイルを生成するか   | true          |
| --timestamps                   |                        | true          |
| --parent=名前                  |                        |               |
| --indexes                      |                        | true          |
| -t, --test-frameword=名前      | 使用するテストフレームワーク       | test_unit     |
| --fixtures                     | フィクスチャを生成するか         | true          |
| -r, --fixture-replacement=名前 | フィクスチャを変更            |               |
| -f, --force                    | ファイルが存在する場合に上書き  |               |
| -q, --quiet                    | 進捗状況を非表示        |               |
| -p, --pretend                  | ドライラン                  |               |
| -s, --skip                     | 既に存在するファイルについてはスキップ |               |
| -h, --help                     | ヘルプを表示               |               |


### カラムの型

データ方     | 説明
----------|---------
string    | 文字列
text      | 長い文字列
integer   | 整数
float     | 浮動小数
decimal   | 精度の高い小数
datetime  | 日時
timestamp | より細かい日時
time      | 時間
date      | 日付
binary    | バイナリデータ
boolean   | Boolean型

### 例
#### userモデルの作成
    $ rails generate model user
          invoke  active_record
          create    db/migrate/YYYYMMDDHHMMSS_create_users.rb
          create    app/models/user.rb
          invoke    test_unit
          create      test/unit/user_test.rb
          create      test/fixtures/users.yml