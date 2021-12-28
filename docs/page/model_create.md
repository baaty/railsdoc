---
layout: page
---

### 説明

モデルを生成して保存  
生成のみしたい場合は、newメソッドを使用

### 使い方

    モデル.create(属性=nil, ブロック引数)

    # 失敗したら例外発生
    モデル.create!(属性=nil, ブロック引数)

### 例

#### モデルを生成して保存

    User.create(name: "TestUser", profile: "profile")

#### whereしてcreate

    users = User.where(name: 'Oscar')
    users.create

#### 属性ハッシュの配列を保存

    User.create([{name: "A"},{name: "B"}])

#### ブロック

    User.create do |user|
        User.name = 'tenderlove'
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation.rb#L95)
