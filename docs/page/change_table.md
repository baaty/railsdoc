---
layout: page
---

### 説明

テーブル定義を変更

### 使い方

    change_table(テーブル名, オプション引数)

### オプション

| オプション | 説明                                   | デフォルト値 |
| ---------- | -------------------------------------- | ------------ |
| :bulk      | 変更内容を1つのALTER TABLEにまとめるか | false        |

### 利用可能なメソッド

| メソッド名                | 説明                                                       |
| ------------------------- | ---------------------------------------------------------- |
| t.primary_key             | プライマリーキーを定義                                     |
| t.column                  | 指定されたテーブルに新しいカラムを追加                     |
| t.index                   | テーブルに新しいインデックスを追加                         |
| t.rename_index            | インデックスの名前を変更                                   |
| t.timestamps              | created_atとupdated_atを両方追加するメソッド               |
| t.change                  | データベースのカラムを変更                                 |
| t.change_default          | カラムに新しいデフォルト値を設定                           |
| t.change_null             | カラムにNOT NULL制約を設定または削除                       |
| t.rename                  | カラムの名前を変更                                         |
| t.references              | 既存のテーブルにリファレンスを追加                         |
| t.belongs_to              | referencesのエイリアス                                     |
| t.check_constraint        | チェック制約を追加                                         |
| t.string                  | String型を定義                                             |
| t.text                    | Text型を定義                                               |
| t.integer                 | Integer型を定義                                            |
| t.bigint                  | Bigint型を定義　                                           |
| t.float                   | Float型を定義                                              |
| t.decimal                 | Decimal型を定義　                                          |
| t.numeric                 | Numeric型を定義                                            |
| t.datetime                | Datetime型を定義                                           |
| t.timestamp               | Timestamp型を定義                                          |
| t.time                    | Time型を定義                                               |
| t.date                    | Date型を定義                                               |
| t.binary                  | Binary型を定義                                             |
| t.boolean                 | Boolean型を定義                                            |
| t.foreign_key             | テーブルに外部キーを追加                                   |
| t.json                    | Join型を定義                                               |
| t.virtual                 | Virtual型を定義                                            |
| t.remove                  | テーブル定義からカラムを削除                               |
| t.remove_foreign_key      | 外部キーをテーブルから削除　                               |
| t.remove_references       | リファレンスを削除                                         |
| t.remove_belongs_to       | remove_referencesのエイリアス                              |
| t.remove_index            | インデックスを削除                                         |
| t.remove_check_constraint | チェック制約をテーブルから削除                             |
| t.remove_timestamps       | テーブルからタイムスタンプ列(created_at、updated_at)を削除 |

### 例

#### pagesテーブルにtext型のmemoを追加、titleにインデックスを設定

    change_table :pages do |t|
      t.text :memo
      t.index :title
    end

#### カラムの追加

    change_table(:suppliers) do |t|
      t.column :name, :string, limit: 60
    end

#### 2つのカラムの追加

    change_table(:suppliers) do |t|
      t.integer :width, :height, null: false, default: 0
    end

#### タイムスタンプを追加

    change_table(:suppliers) do |t|
      t.timestamps
    end

#### 外部キーを追加

    change_table(:suppliers) do |t|
      t.references :company
    end

#### 複数カラムの削除

    change_table(:suppliers) do |t|
      t.remove :company_id
      t.remove :width, :height
    end

#### インデックスを削除

    change_table(:suppliers) do |t|
      t.remove_index :company_id
    end

### メソッド詳細

#### t.primary_key

##### 説明

プライマリーキーを定義

##### 使い方

    primary_key(名前, タイプ=:primary_key, オプション引数)

##### 例

    t.primary_key :id, :uuid, default: "uuid_generate_v4()"

##### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/postgresql/schema_definitions.rb#L48)

#### t.column

##### 説明

指定されたテーブルに新しいカラムを追加

##### 使い方

    column(カラム名, 型, index: インデックス=nil, オプション引数)

##### 例

    t.column(:name, :string)

##### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L624)

#### t.index

##### 説明

テーブルに新しいインデックスを追加

##### 使い方

    index(カラム名, オプション引数)

##### 例

    t.index(:name)
    t.index([:branch_id, :party_id], unique: true)
    t.index([:branch_id, :party_id], unique: true, name: 'by_branch_party')

##### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L649)

#### t.rename_index

##### 説明

インデックスの名前を変更

##### 使い方

    rename_index(インデックス名, 新しいインデックス名)

##### 例

    t.rename_index(:user_id, :account_id)

##### ソースコード

- [GitHub](https://github.com/rails/rails/blob/83217025a171593547d1268651b446d3533e2019/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L644)

#### t.timestamps

##### 説明

created_atとupdated_atを両方追加するメソッド

##### 使い方

    timestamps(オプション引数)

##### 例

##### usersテーブルにtimestampsを設定

    create_table :users do |t|
      t.timestamps
    end

##### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L406)

#### t.change

##### 説明

データベースのカラムを変更

##### 使い方

    change(カラム名, 型, オプション引数)

##### オプション

| オプション | 説明                                                           | デフォルト値 |
| ---------- | -------------------------------------------------------------- | ------------ |
| :limit     | カラムの桁数を指定                                             |              |
| :default   | デフォルト値を指定                                             |              |
| :null      | NULL値を許可するか                                             | true         |
| :precision | :decimal、:numeric、:datetime、および:time型の精度を指定       |              |
| :scale     | :decimal、:numeric型の小数点以下の桁数                         |              |
| :collation | :stringまたは：textの照合順序を指定                            |              |
| :comment   | カラムのコメントを指定。データベース管理ツールなどで閲覧が可能 |              |

##### 例

###### データベースのカラムを変更

    t.change(:description, :text)

###### カラムの桁数を指定して変更

    t.change(:name, :string, limit: 80)

##### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L688)

#### t.change_default

##### 説明

カラムに新しいデフォルト値を設定

##### 使い方

    change_default(カラム, デフォルト値)

##### 例

    t.change_default(:qualification, 'new')
    t.change_default(:authorized, 1)
    t.change_default(:status, from: nil, to: "draft")

##### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L699)

#### t.change_null

##### 説明

カラムにNOT NULL制約を設定または削除

##### 使い方

    change_null(カラム, NULL, デフォルト値=nil)

##### 例

    t.change_null(:qualification, true)
    t.change_null(:qualification, false, 0)

##### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L709)

#### t.rename

##### 説明

カラムの名前を変更

##### 使い方

    rename(カラム名, 新しいカラム名)

##### 例

    t.rename(:description, :name)

##### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L749)

#### t.references

##### 説明

既存のテーブルにリファレンスを追加

##### 使い方

    references(カラム名 [, オプション])

##### オプション

| オプション   | 説明                   | デフォルト値 |
| ------------ | ---------------------- | ------------ |
| :type        | カラムタイプ           | :bigint      |
| :index       | インデックスを付与     | true         |
| :foreign_key | 外部キーの制約         | false        |
| :polymorphic | ポリモーフィックを付与 | false        |
| :null        | NULLを許可するか       | true         |

##### 例

    t.references(:user)

##### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L478)

#### t.check_constraint

##### 説明

チェック制約を追加

##### 使い方

    check_constraint(引数..)

##### 例

    t.check_constraint("price > 0", name: "price_check")

##### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L813)

#### t.string

##### 説明

String型を定義

##### 使い方

    t.string(カラム名)

##### 例

    t.string(:name)

#### t.text

##### 説明

Text型を定義

##### 使い方

    t.text(カラム名)

##### 例

    t.text(:name)

#### t.integer

##### 説明

Integer型を定義

##### 使い方

    t.integer(カラム名)

##### 例

    t.integer(:age)

#### t.bigint

##### 説明

Bigint型を定義

##### 使い方

    t.bigint(カラム名)

##### 例

    t.bigint(:num)

#### t.float

##### 説明

Float型を定義

##### 使い方

    t.float(カラム名)

##### 例

    t.float(:num)

#### t.decimal

##### 説明

Decimal型を定義

##### 使い方

    t.decimal(カラム名)

##### 例

    t.decimal(:num)

#### t.numeric

##### 説明

Numeric型を定義

##### 使い方

    t.numeric(カラム名)

##### 例

    t.numeric(:num)

#### t.datetime

##### 説明

Datetime型を定義

##### 使い方

    t.datetime(カラム名)

##### 例

    t.datetime(:time)

#### t.timestamp

##### 説明

Timestamp型を定義

##### 使い方

    t.timestamp(カラム名)

##### 例

    t.timestamp(:time)

#### t.time

##### 説明

Time型を定義

##### 使い方

    t.time(カラム名)

##### 例

    t.time(:time)

#### t.date

##### 説明

Date型を定義

##### 使い方

    t.date(カラム名)

##### 例

    t.date(:date)

#### t.binary

##### 説明

Binary型を定義

##### 使い方

    t.binary(カラム名)

##### 例

    t.binary(:image)

#### t.boolean

##### 説明

Boolean型を定義

##### 使い方

    t.boolean(カラム名)

##### 例

    t.boolean(:flag)

#### t.foreign_key

##### 説明

テーブルに外部キーを追加

##### 使い方

    foreign_key(引数, オプション引数)

##### 例

    t.foreign_key(:authors)
    t.foreign_key(:authors, column: :author_id, primary_key: "id")

##### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L785)

#### t.json

##### 説明

Json型を定義

##### 使い方

    t.json(カラム名)

##### 例

    t.json(:request)

#### t.virtual

##### 説明

Virtual型を定義

##### 使い方

    t.virtual(カラム名)

##### 例

    t.virtual(:hoge)

#### t.remove

##### 説明

テーブル定義からカラムを削除

##### 使い方

    remove(カラム名.., オプション引数)

##### 例

    t.remove(:qualification)
    t.remove(:qualification, :experience)

##### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L719)

#### t.remove_foreign_key

##### 説明

外部キーをテーブルから削除

##### 使い方

    remove_foreign_key(外部キー.., オプション引数)

##### 例

    t.remove_foreign_key(:authors)
    t.remove_foreign_key(column: :author_id)

##### ソースコード

- [GitHub](https://github.com/rails/rails/blob/83217025a171593547d1268651b446d3533e2019/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L770)

#### t.remove_references

##### 説明

リファレンスを削除

##### 使い方

    remove_reference(テーブル名, リファレンス名, foreign_key: 外部キー=false, polymorphic: ポリモーフィック=false, オプション引数)

##### 例

    t.remove_references(:user)

##### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L772)

#### t.remove_index

##### 説明

インデックスを削除

##### 使い方

    t.rremove_index(カラム名=nil, オプション引数)

##### 例

    t.remove_index(:user)

##### ソースコード

- [GitHub](https://github.com/rails/rails/blob/83217025a171593547d1268651b446d3533e2019/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L706)

#### t.remove_check_constraint

##### 説明

チェック制約をテーブルから削除

##### 使い方

    t.remove_check_constraint(引数..)

##### 例

    t.remove_check_constraint(name: "price_check")

##### ソースコード

- [GitHub](https://github.com/rails/rails/blob/83217025a171593547d1268651b446d3533e2019/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L797)

#### t.remove_timestamps

##### 説明

テーブルからタイムスタンプ列(created_at、updated_at)を削除

##### 使い方

t.remove_timestamps(オプション引数)

##### 例

    t.remove_timestamps

##### ソースコード

- [GitHub](https://github.com/rails/rails/blob/83217025a171593547d1268651b446d3533e2019/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L715)
