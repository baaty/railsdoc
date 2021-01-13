---
layout: page
---
### 説明
参照元テーブルから参照先テーブルにアクセスする

### 使い方
#### rails3
    belongs_to(関連モデル名 [, オプション])

#### rails4
    belongs_to(関連モデル名 [, scope, オプション])

### オプション

オプション          | 説明                                                            | デフォルト
-------------- | ------------------------------------------------------------- | -------------
:class_name    | 関連を設定するモデルクラス名を指定。関連名と参照先のクラス名を異なるものにしたい場合に指定                 |
:foreign_key   | 参照先を参照するための外部キーの名前を指定                                         | :foreign_key
:foreign_type  | 参照先を参照するための外部キーの型を指定                                          | :foreign_type
:primary_key   | 主キーを指定                                                        | id
:dependent     | 値を:destroyにすると、参照先が削除される場合に参照元もDBから削除                         |
:counter_cache | trueにすると、カウンタキャッシュを使用                                         |
:polymorphic   | ポリモーフィック関連を定義                                                 |
:validate      | 関連オブジェクトの検証の有無                                                | false
:autosave      | trueにすると、親のオブジェクトが保存されると、ロードされたオブジェクトも保存                      |
:touch         | trueにすると、updated_atまたはupdated_onがオブジェクトが保存または破棄された場合に現在の時刻を設定 |
:inverse_of    | 関連を指定                                                         |
:required      |                                                               |

### 追加されているメソッド

メソッド                                 | 説明
------------------------------------ | ------------------------------------------------------------
association(force_reload = false)    | 自分自身を参照しているオブジェクトを返す。オブジェクトが無い場合は、nilを返す
association=(associate)              | 引数を参照元オブジェクトとして設定。それ以外の参照元との関連は破棄
build_association(attributes = {})   | 新しいオブジェクトを生成。引数にはオブジェクトを生成するのに必要なパラメータを指定。この時点では保存されない
create_association(attributes = {})  | 新しいオブジェクトを生成して保存。引数にはオブジェクトを生成するのに必要なパラメータを指定
create_association!(attributes = {}) | 新しいオブジェクトを生成して保存。引数にはオブジェクトを生成するのに必要なパラメータを指定。失敗時に例外を発生

### 保存
#### 参照元オブジェクトが未保存の場合
* saveのタイミングで外部キーが設定され保存
* 参照先オブジェクトが未保存であれば、saveのタイミングで自動的に保存

#### 参照元オブジェクトが保存済みの場合
* 保存済みの場合には、生成したタイミングで自動的にDBに保存

### 例
#### UserとProjectの関係
##### Projectモデル
    class Project < ActiveRecord::Base
    &nbsp;&nbsp;belongs_to :user
    end

#### クラス名としてUserを指定
    belongs_to :admin_user, :class_name => "User"

#### user_id = 2を抽出
    belongs_to :user, :conditions => "user_id = 2"

#### 逆順で並び替える
    belongs_to :user, :order => "id DESC"

#### データを削除するときに関連するテーブルを削除
    belongs_to :user, :dependent => :destroy

#### 外部キーを指定
    belongs_to :user, foreign_key => "blog_id"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0af3dd4438047d8c5783dff1cfcf9c696b44bdff/activerecord/lib/active_record/associations.rb#L1514)
