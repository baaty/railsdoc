---
layout: page
---

### 説明

モデルオブジェクトを生成  
保存はまだされていないため、saveメソッドなどを使って保存  
生成と同時に保存したい場合は、createメソッドを使用

### 使い方

    モデル.new(属性={})

### 例

#### モデルオブジェクトを生成

    User.new

#### 属性を指定

    User.new(name: "DHH")

#### 複数属性を指定

    User.new(name: 'bob', age: '18')

#### ブロックで指定

    users.new do |user|
      user.name = 'Oscar'
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/model.rb)
