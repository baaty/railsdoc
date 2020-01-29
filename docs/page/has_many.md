---
layout: page
---
### 説明
1対多や多対多の関連付けを指定

### 使い方
    has_many(関連モデル名 [, scope, オプション])

### オプション

オプション       | 説明
-------------- | ----
:class_name    | 関連名と参照元のクラス名を異なるものにしたい場合に指定
:foreign_key   | 参照元のテーブルに定義されている外部キーの名前を指定
:foreign_type  | オブジェクトタイプを指定
:primary_key   | 参照先のテーブルに定義されている外部キーの名前を指定
:dependent     | 値を:destroyにすると、参照先が削除される場合に参照元もDBから削除
:counter_cache | カウンターキャッシュ
:as            | ポリモーフィック関連を定義
:through       | 結合モデルの指定
:source        | has_one :through の元となるオブジェクトを指定
:source_type   | polymorphicの指定
:validate      | オブジェクトが保存されると、バリデイトが実行される
:autosave      | 親のオブジェクトが保存されると、ロードされたオブジェクトも保存
:inverse_of    | モデル名を指定
:extend        | 関連を拡張

### 追加されるメソッド

メソッド                              | 説明
------------------------------------ | ----------------------------
collection(force_reload = false)     | 関連付けられている配列
collection<<(object, …)              | collectionにobjectを追加
collection.delete(object, …)         | 1つ以上のobjectを削除
collection.destroy(object, …)        | 1つ以上のobjectを削除
collection=objects                   | 多対多でひも付いたモデルを更新
collection_singular_ids              | 関連付けられているオブジェクトのIDの配列
collection_singular_ids=ids          | 主キーを切り替える
collection.clear                     | すべて切断
collection.empty?                    | オブジェクトが関連付けられていなければtrue
collection.size                      | サイズ
collection.find(…)                   | 通常のfindメソッド
collection.exists?(…)                | 与えられた条件に一致するモデルが存在するか確認
collection.build(attributes = {}, …) | 新しいモデルを作り、多対多で関連付けるがDBは更新しない
collection.create(attributes = {})   | 新しいモデルを作り、多対多で関連付けてDBを更新
collection.reload                    | リロード

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
        create_table :users_projects, id: false do |t|
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
    has_many :admin_user, class_name: "User"
    accepts_nested_attributes_for :admin_user

#### user_id = 2を抽出
    has_many :user, conditions: "user_id = 2"
    accepts_nested_attributes_for :user

#### 逆順で並び替える
    has_many :user, order: "id DESC"
    accepts_nested_attributes_for :user

#### Group
    has_many :users, group: "category"
    accepts_nested_attributes_for :users

#### 外部キーを指定
    has_many :user, foreign_key: "blog_id"
    accepts_nested_attributes_for :user

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/associations.rb#L1370)