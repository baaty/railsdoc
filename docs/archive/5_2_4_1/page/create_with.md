---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/query_methods.rb#L768)