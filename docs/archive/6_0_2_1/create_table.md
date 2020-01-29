---
layout: page
---
### 説明
テーブルを作成

### 使い方
    create_table(テーブル名 [, オプション])

    create_table テーブル名  [, オプション] do |t|
      t.型 カラム名 [, カラムオプション]
    end

### オプション

オプション          | 説明                        | デフォルト値
---------------|-----------------------------|-------
:id            | 主キーを自動生成               | true
:primary_key   | 主キーのカラムの名前               | id
:options       | テーブルオプション                   |
:temporary     | 一時テーブルとして作成             | false
:force         | テーブルを作成前に、既存のテーブルを削除 | false
:if_not_exists | テーブルが存在するときにエラーにしない       | false
:as            | テーブル作成時に使うSQL           |

### カラムオプション

オプション      | 説明            | デフォルト値
-----------|----------------|-------
:limit     | カラムの桁数        |
:default   | デフォルトの値        |
:null      | nullを許可するか    | true
:precision | 数値の桁数       |
:scale     | 小数点以下の桁数 |

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
#### テーブルの作成
    crate_table :products do |t|
      t.string :name
    end

#### 空のカラムを禁止
    create_tabe :products |t|
      t.string :name, null: false
    end

#### 文字コードを指定してテーブルを作成
    create_table :suppliers, options: 'ENGINE=InnoDB DEFAULT CHARSET=utf8'

#### 主キーを指定してテーブルを作成
    create_table(:objects, primary_key: 'guid') do |t|
      t.column :name, :string, limit: 80
    end

#### プライマリーキーの無いテーブルを作成
    create_table(:categories_suppliers, id: false) do |t|
      t.column :category_id, :integer
      t.column :supplier_id, :integer
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L294)