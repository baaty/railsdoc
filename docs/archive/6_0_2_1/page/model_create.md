---
layout: page
---
### 説明
モデルオブジェクトを生成して保存  
生成のみしたい場合は、newメソッドを使用

### 使い方
    モデル.create([属性])

#### 失敗したら例外
    モデル.create!([属性])

### 例
#### モデルを生成して保存
    User.create(name: "TestUser", profile: "profile")

#### 属性ハッシュの配列を保存
    User.create([{name: "A"},{name: "B"}])

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation.rb#L95)