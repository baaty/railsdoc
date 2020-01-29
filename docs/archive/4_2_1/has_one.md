---
layout: page
---
### 説明
指定のクラスがこのクラスの子であることを宣言

### 使い方
#### rails3
    has_one(関連モデル名, [オプション])

#### rails4
    has_one(関連モデル名 [, scope ,オプション])

### オプション

オプション        | 説明                                       | バージョン
------------ | ---------------------------------------- | --------
:class_name  | 関連名と参照元のクラス名を異なるものにしたい場合に指定              |
:dependent   | 値を:destroyにすると、参照先が削除される場合に参照元もDBから削除    |
:foreign_key |                                          |
:primary_key | 参照先のテーブルに定義されている外部キーの名前を指定               |
:as          | ポリモーフィック関連を定義                            |
:through     | 結合モデルの指定                                 |
:source      | has_one :throughの元となるオブジェクトを指定           |
:source_type | polymorphicの指定                           |
:validate    | オブジェクトが保存されると、バリデイトが実行される                |
:autosave    | 親のオブジェクトが保存されると、ロードされたオブジェクトも保存          |
:inverse_of  |                                          |
:conditions  | 参照元を検索する際の条件を設定。SQLのWHERE句にしている案件を文字列で定義 | rails3まで
:include     | 関連モデルクラスのオブジェクトをロードする際、同時に読み込みたいモデルを指定   | rails3まで
:order       | 関連をロードする際のソート順を設定                        | rails3まで
:readonly    | 読み込み専用のオブジェクトを生成したい場合はtrueを指定            | rails3まで
:select      | カラムの指定                                   | rails3まで

### 追加されるメソッド

メソッド                                 | 説明
------------------------------------ | -------------------------------------------------------------
association(force_reload = false)    | 自分自身を参照しているオブジェクトを返す。オブジェクトが無い場合は、nilを返す
association=(associate)              | 引数を参照元オブジェクトとして設定。それ以外の参照元との関連は破棄
build_association(attributes = {})   | 新しいオブジェクトを作成。引数にはオブジェクトを生成するのに必要なパラメータを指定。この時点では保存されない
create_association(attributes = {})  | 新しいオブジェクトを作成して保存。引数にはオブジェクトを生成するのに必要なパラメータを指定
create_association!(attributes = {}) | 新しいオブジェクトを作成して保存。引数にはオブジェクトを生成するのに必要なパラメータを指定。エラー時に例外を発生

### 保存
#### 参照先オブジェクトが未保存の場合
* saveのタイミングで外部キーが設定され保存
* 参照先オブジェクトが未保存であれば、saveのタイミングで自動的に保存

#### 参照先オブジェクトが保存済みの場合
* 保存済みの場合には、作成するタイミングで自動的にDBに保存

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
     vend
    end

##### Userモデル
    class User < ActiveRecord::Base
      has_one :project
    end

##### Projectモデル
    class Project < ActiveRecord::Base
      belongs_to :user
    end

#### クラス名としてUserを指定
    has_one :admin_user, :class_name => "User"

#### user_id = 2を抽出
    has_one :user, :conditions => "user_id = 2"

#### 逆順で並び替える
    has_one :user, :order => "id DESC"

#### データを削除するときに関連するテーブルを削除
    has_one :user, :dependent => :destroy

#### 外部キーを指定
    has_one :user, foreign_key => "blog_id"