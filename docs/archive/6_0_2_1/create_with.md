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
    users.new.name
    # 'Oscar'

    users = users.create_with(name: 'DHH')
    users.new.name
    # 'DHH'

#### 属性をリセット
    users = users.create_with(nil)
    users.new.name
    # 'Oscar'

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/query_methods.rb#L836)