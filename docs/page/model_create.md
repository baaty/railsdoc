---
layout: page
---
### 説明
モデルオブジェクトを生成して保存
生成のみを行いたい場合は、newメソッドを使用

### 使い方
    モデル.create([属性])

### 例
#### 基本的な使い方
    user = User.create(name: "TestUser", profile: "profile")

#### 属性ハッシュの配列を保存
    user = User.create([{name: "A"},{name: "B"}])

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation.rb#L95)