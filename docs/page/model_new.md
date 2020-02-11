---
layout: page
---
### 説明
モデルオブジェクトを生成  
保存はまだされていないため、saveメソッドなどを使って保存  
生成と同時に保存したい場合は、createメソッドを使用

### 使い方
    モデル.new([属性])

### 例
#### モデルオブジェクトを生成
    User.new
    # <User id: nil, created_at: nil, updated_at: nil>

#### 属性を指定
    User.new(name: "DHH")
    # <User id: nil, name: "DHH", created_at: nil, updated_at: nil>

#### ブロックで指定
    users.new do |user|
      user.name = 'Oscar'
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation.rb#L69)