---
layout: page
---

### 説明

関連モデルオブジェクトから新しい属性を作成  
「nil」を引数で渡すと属性をリセット

### 使い方

    モデル.create_with(属性)

### 例

#### 関連オブジェクトから新しいモデルを作成

    users = users.create_with(name: 'DHH')
    users.new.name
    # 'DHH'

#### 属性をリセット

    users = users.create_with(nil)
    users.new.name
    # 'Oscar'

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L1003)
