---
layout: page
---
### 説明
指定したテーブルにカラムを追加

### 使い方
    add_column(テーブル名 カラム名, タイプ [, オプション])


### オプション

オプション      | 説明                  | デフォルト
---------- | ------------------- | -----
:limit     | カラムの桁数を指定           |
:default   | デフォルト値を指定           |
:null      | nill値を許可するか         | true
:precision | :decimal 型の精度を指定    |
:scale     | :decimal 型の小数点以下の桁数 |

precisionとscaleについては、データベースによって差があるので注意が必要

### 例
#### postsテーブルにtitleカラムを作成
    def self.up
        add_column :posts, :title, :string
    end

#### カラムの桁数が10桁
    def self.up
        add_column :posts, :title, :string, :limit => 10
    end

#### null値を許可しない
    def self.up
        add_column :posts, :title, :string, :null => false
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/9985da0856bad47d25a0bf6cc34474cd69f1b77c/activerecord/lib/active_record/connection_adapters/postgresql/schema_statements.rb#L423)