---
layout: page
---
### 説明
関連オブジェクトから新しいモデルを作成
「nil」を引数で渡すと属性をリセットすることができる

### 使い方
    モデル.create_with(属性)

### 例
#### 関連オブジェクトから新しいモデルを作成
    users = User.where(name: 'Oscar')
    users.new.name # => 'Oscar'

    users = users.create_with(name: 'DHH')
    users.new.name # => 'DHH'

#### 属性をリセット
    users = users.create_with(nil)
    users.new.name # => 'Oscar'

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0399b71dab8b270b4e40b2aff99194a8b8f2596c/activerecord/lib/active_record/relation/query_methods.rb#L726)