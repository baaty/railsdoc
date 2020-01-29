---
layout: page
---
### 説明
1対多や多対多の関係を表現するときに使用

### 使い方
#### rails3
    has_many(関連モデル名 [, オプション])
     accepts_nested_attributes_for 関連モデル名

#### rails4
    has_many(関連モデル名 [, scope, オプション])
     accepts_nested_attributes_for 関連モデル名

### オプション

オプション          | 説明                                                                                                                                                                                                                                                                                             | バージョン
-------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------
:class_name    | 関連名と参照元のクラス名を異なるものにしたい場合に指定                                                                                                                                                                                                                                                                    |
:foreign_key   | 参照元のテーブルに定義されている外部キーの名前を指定                                                                                                                                                                                                                                                                     |
:primary_key   | 参照先のテーブルに定義されている外部キーの名前を指定                                                                                                                                                                                                                                                                     |
:dependent     | 値を:destroyにすると、参照先が削除される場合に参照元もDBから削除                                                                                                                                                                                                                                                          |
:counter_cache | カウンターキャッシュ                                                                                                                                                                                                                                                                                     | rails4以降
:as            | ポリモーフィック関連を定義                                                                                                                                                                                                                                                                                  |
:through       | 結合モデルの指定                                                                                                                                                                                                                                                                                       |
:source        | has_one :through の元となるオブジェクトを指定                                                                                                                                                                                                                                                                |
:source_type   | polymorphicの指定                                                                                                                                                                                                                                                                                 |
:validate      | オブジェクトが保存されると、バリデイトが実行される                                                                                                                                                                                                                                                                      |
:autosave      | 親のオブジェクトが保存されると、ロードされたオブジェクトも保存                                                                                                                                                                                                                                                                |
:inverse_of    | Specifies the name of the belongs_to association on the associated object that is the inverse of this has_many association. Does not work in combination with :through or :as options. See ActiveRecord::Associations::ClassMethods's overview on Bi-directional associations for more detail. |
:conditions    | 参照元を検索する際の条件を設定すSQLのWHERE句にしている案件を文字列で定義                                                                                                                                                                                                                                                       | rails3まで
:counter_sql   | 関連の大きさを指定するためのSQL文を指定                                                                                                                                                                                                                                                                          | rails3まで
:extend        | プロキシを拡張するためのモジュール                                                                                                                                                                                                                                                                              | rails3まで
:finder_sql    | 関連を取得SQL文を指定                                                                                                                                                                                                                                                                                   | rails3まで
:group         | グルーピング命令                                                                                                                                                                                                                                                                                       | rails3まで
:include       | 関連モデルクラスのオブジェクトをロードする際、同時に読み込みたいモデルを指定                                                                                                                                                                                                                                                         | rails3まで
:limit         | 取得件数                                                                                                                                                                                                                                                                                           | rails3まで
:offset        | オフセット値                                                                                                                                                                                                                                                                                         | rails3まで
:order         | 関連をロードする際のソート順を指定。SQLのORDER BY句に指定する条件を文字列で定義                                                                                                                                                                                                                                                  | rails3まで
:readonly      | 読み込み専用のオブジェクトを生成したい場合はtrueを指定                                                                                                                                                                                                                                                                  | rails3まで
:select        | カラムの指定                                                                                                                                                                                                                                                                                         | rails3まで
:uniq          | 重複した関連を無視するか                                                                                                                                                                                                                                                                                   | rails3まで

### 追加されるメソッド

メソッド                                 | 説明                           | バージョン
------------------------------------ | ---------------------------- | --------
collection(force_reload = false)     | 関連付けられている配列を返す               |
collection<<(object, …)              | collectionにobjectを追加         |
collection.delete(object, …)         | 1つ以上のobjectを削除               |
collection.destroy(object, …)        | 1つ以上のobjectを削除               | rails4以降
collection=objects                   | 多対多でひも付いたモデルを更新              |
collection_singular_ids              | 関連付けられているオブジェクトのIDの配列を返す     |
collection_singular_ids=ids          | 主キーを切り替える                    |
collection.clear                     | すべて切断                        |
collection.empty?                    | オブジェクトが関連付けられていなければtrueを返す   |
collection.size                      | サイズを返す                       |
collection.find(…)                   | 通常のfindメソッド                  |
collection.exists?(…)                | 与えられた条件に一致するモデルが存在するか確認      |
collection.build(attributes = {}, …) | 新しいモデルを作り、多対多で関連付けるがDBは更新しない |
collection.create(attributes = {})   | 新しいモデルを作り、多対多で関連付けてDBを更新     |

### 保存
#### 参照先オブジェクト、参照元オブジェクトのどちらかが未保存の場合
* saveのタイミングで両方とも保存

#### 参照先オブジェクト、参照元オブジェクトの保存済みの場合
* 参照元オブジェクトの外部キーが更新され、保存

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
      has_many :projects
      accepts_nested_attributes_for :projects
    end

##### Projectモデル
    class Project < ActiveRecord::Base
      belongs_to :user
      accepts_nested_attributes_for :user
    end

#### クラス名としてUserを指定
    has_many :admin_user, :class_name => "User"
    accepts_nested_attributes_for :admin_user

#### user_id = 2を抽出
    has_many :user, :conditions => "user_id = 2"
    accepts_nested_attributes_for :user

#### 逆順で並び替える
    has_many :user, :order => "id DESC"
    accepts_nested_attributes_for :user

#### Group
    has_many :users, :group => "category"
    accepts_nested_attributes_for :users

#### 外部キーを指定
    has_many :user, foreign_key => "blog_id"
    accepts_nested_attributes_for :user

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0af3dd4438047d8c5783dff1cfcf9c696b44bdff/activerecord/lib/active_record/associations.rb#L1258)