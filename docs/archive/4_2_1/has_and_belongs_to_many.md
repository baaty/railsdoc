---
layout: page
---
### 説明
多対多の関連を表現するときに使用

### 使い方
#### rails3
    has_and_belongs_to_many(関連モデル名 [, オプション])

#### rails4
    has_and_belongs_to_many(関連モデル名 [, scope, オプション])

### オプション

オプション                    | 説明                                   | バージョン
------------------------ | ------------------------------------ | --------
:class_name              | 関連モデルのクラス名を指定
関連モデル名から推測できない場合のみ指定 |
:join_table              | 結合テーブルの名前を指定                         |
:foreign_key             | 多対多の関連で使用する外部キーの名前を指定                |
:association_foreign_key | 多対多の関係で関連先への外部キーを指定                  |
:readonly                | 関連先のオブジェクトを読み取り専用にするか                |
:validate                | 現在のモデルを保存する場合、関連先の検証を実行              |
:autosave                | 親モデルに合わせて、保存や削除を行うか                  |
:conditions              | 関連モデルを取得する際の条件式を指定                   | rails3まで
:counter_sql             | 関連の大きさを指定するためのSQL文を指定                | rails3まで
:delete_sql              | 関連を削除するためのSQL文を指定                    | rails3まで
:extend                  | プロキシを拡張するためのモジュール                    | rails3まで
:finder_sql              | 関連を取得SQL文を指定                         | rails3まで
:group                   | 結果をグループ化                             | rails3まで
:include                 | 2次の関連も取得するか                          | rails3まで
:insert_sql              | 関連を追加するためのSQL文を指定                    | rails3まで
:limit                   | 取得する関連モデルの上限を指定                      | rails3まで
:offset                  | 取得する関連モデルの開始位置を指定                    | rails3まで
:order                   | 関連先オブジェクトの取得順序を指定                    | rails3まで
:select                  | 関連先オブジェクトの取得例を指定                     | rails3まで
:uniq                    | 重複した関連を無視するか                         | rails3まで

### 使えるようになるメソッド

メソッド                               | 説明
---------------------------------- | ----------------------------
collection(force_reload = false)   | 多対多でひも付いた先のモデルである一覧を取得
collection<<(object, …)            | 1つ以上のモデルを多対多の関連に追加
collection.delete(object, …)       | 1つ以上のモデルを多対多の関連から外す
collection.destroy(object, …)      | 1つ以上のモデルを多対多の関連から外す
collection=objects                 | 多対多でひも付いたモデルを更新
collection_singular_ids            | 多対多でひも付いたモデルのidの配列を取得
collection_singular_ids=ids        | 多対多でひも付いたモデルのidが指定された物に更新
collection.clear                   | 多対多の関連をすべて削除
collection.empty?                  | 多対多の関連にあるモデルが1つもないときにtrue
collection.size                    | 多対多でひも付いたモデル数を返す
collection.find(id)                | 多対多の関連モデルでfindを実行
collection.exists?(…)              | 与えられた条件に一致するモデルが存在するか確認
collection.build(attributes = {})  | 新しいモデルを作り、多対多で関連付けるがDBは更新しない
collection.create(attributes = {}) | 新しいモデルを作り、多対多で関連付けてDBを更新

### 例
#### UserとProjectの関係
##### マイグレーションファイル
    class CreateUsersProjectsTable < ActiveRecord::Migration
      def self.up
        create_table :users_projects, :id => false do |t|
          t.integer :user_id
          t.integer :project_id
        end
      end
      def self.down
        drop_table :users_projects
      end
    end

##### Userモデル
    class User < ActiveRecord::Base
      has_and_belongs_to_many :projects
    end

##### Projectモデル
    class Project < ActiveRecord::Base
      has_and_belongs_to_many :users
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0af3dd4438047d8c5783dff1cfcf9c696b44bdff/activerecord/lib/active_record/associations.rb#L1679)