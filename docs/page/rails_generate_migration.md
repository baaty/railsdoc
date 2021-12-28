---
layout: page
---

### 説明

マイグレーションファイル(テーブル定義の作成・変更するファイル)を生成

### 特徴

- 必ずupメソッドとdownメソッドを含めなければならない
- self.upがmigrationのバージョンがあがるときに実行
- self.downがmigrationのバージョンがあがるときに実行
- クラス名をすべて小文字にしたものが、ファイル名アンダースコア(\_)以降と一致する必要がある

### 使い方

    $ rails generate migration 名前 [カラム名:型[:index]..] [オプション]

### オプション

| オプション                          | 説明                                   | デフォルト値 |
| ----------------------------------- | -------------------------------------- | ------------ |
| --skip-namespace                    | namespaceの生成をスキップ              |              |
| --skip-collision-check              | コリジョンチェックをスキップ           |              |
| --timestamps                        | timestampsファイルを生成するか         | true         |
| --primary-key-type=PRIMARY_KEY_TYPE | 主キーのタイプ                         |              |
| -d, --database=DATABASE             | データベースの種類                     | sqlite3      |
| -f, --force                         | ファイルが存在する場合に上書き         |              |
| -q, --quiet                         | 進捗状況を表示しない                   |              |
| -p, --pretend                       | ドライラン                             |              |
| -s, --skip                          | 既に存在するファイルはスキップ |              |
| -h, --help                          | ヘルプを表示                           |              |

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

### 作成されるファイルの基本構成

    class マイグレーション名s < ActiveRecord::Migration
      def up
      end

      def down
      end
    end

### 例

#### マイグレーションファイルを生成

    $ rails generate migration Page

#### カラムを指定して生成

    $ rails generate migration AddTitleToPage title:string
