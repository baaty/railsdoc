---
layout: page
---

### 説明

参照元テーブルから参照先テーブルを参照するための設定

### 使い方

    belongs_to(関連モデル名, scope=nil, オプション={})

### オプション

| オプション          | 説明                                                                         | デフォルト値  |
| ------------------- | ---------------------------------------------------------------------------- | ------------- |
| :class_name         | 関連を設定するモデル名を指定                                                 |               |
| :foreign_key        | 参照先を参照するための外部キーの名前を指定                                   | :foreign_key  |
| :foreign_type       | 参照先を参照するための外部キーの型を指定                                     | :foreign_type |
| :primary_key        | 主キーを指定                                                                 | id            |
| :dependent          | :destroyで参照先が削除される場合に参照元もDBから削除                         |               |
| :counter_cache      | カウンタキャッシュを使用するか                                               |               |
| :polymorphic        | ポリモーフィック関連を定義                                                   |               |
| :validate           | 関連オブジェクトのバリデーションの有無                                       | false         |
| :autosave           | 親の保存でロードされたオブジェクトも保存するか                               |               |
| :touch              | updated_atまたはupdated_onが保存または破棄された場合に現在の時刻を設定するか |               |
| :inverse_of         | モデルを指定                                                                 |               |
| :optional           | 関連付けの確認は行わないか？                                                 |               |
| :required           | 関連付けの確認するか？                                                       | true          |
| :default            | 特定のカラムの初期化                                                         |               |
| :strict_loading     | 厳格な読み込みを実施                                                         |               |
| :ensuring_owner_was | 呼び出されるインスタンスメソッドを指定                                       |               |

### 追加されているメソッド

| メソッド                             | 説明                                                                                                           |
| ------------------------------------ | -------------------------------------------------------------------------------------------------------------- |
| association                          | 関連するオブジェクトを生成                                                                                     |
| association=(associate)              | 引数を参照元オブジェクトとして設定。それ以外の参照元との関連は破棄                                             |
| build_association(attributes = {})   | 新しいオブジェクトを生成。引数にはオブジェクトを生成するのに必要なパラメータを指定。この時点では保存されない   |
| create_association(attributes = {})  | 新しいオブジェクトを生成して保存。引数にはオブジェクトを生成するのに必要なパラメータを指定                     |
| create_association!(attributes = {}) | 新しいオブジェクトを生成して保存。引数にはオブジェクトを生成するのに必要なパラメータを指定。失敗時に例外を発生 |
| reload_association                   | キャッシュではなくデータベースから直接値を取得                                                                 |
| association_changed?                 | 新しいオブジェクトが割り当てられ、次の保存で外部キーが更新される場合はtrue                                     |
| association_previously_changed?      | 前回の保存で新しいオブジェクトを参照するように更新された場合true                                               |

### 保存

#### 参照元オブジェクトが未保存の場合

- saveのタイミングで外部キーが設定され保存
- 参照先オブジェクトが未保存であれば、saveのタイミングで自動的に保存

#### 参照元オブジェクトが保存済みの場合

- 保存済みの場合には、生成したタイミングで自動的にDBに保存

### 例

#### UserとProjectの関係

##### 基本形(オプションなし)

    belongs_to :user

#### クラス名としてUserを指定

    belongs_to :admin_user, class_name: "User"

#### user_id = 2を抽出

    belongs_to :user, conditions: "user_id = 2"

#### 逆順で並び替える

    belongs_to :user, order: "id DESC"

#### データを削除するときに関連するテーブルを削除

    belongs_to :user, dependent: :destroy

#### 外部キーを指定

    belongs_to :user, foreign_key: "blog_id"

#### 特定のキーの初期化

    belongs_to :account, default: -> { company.account }

### ソースコード

    * [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/associations.rb#L769)
