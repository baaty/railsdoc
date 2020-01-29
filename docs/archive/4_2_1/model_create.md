---
layout: page
---
### 説明
モデルオブジェクトを生成して保存
生成のみを行いたい場合は、newメソッドを使用

### 使い方
    モデル.create([属性])

### 例
#### 基本的な使い方(Ruby1.8 & 1.9)
    user = User.create(:name => "TestUser", :profile => "profile")

#### 基本的な使い方(Ruby1.9)
    user = User.create(name: "TestUser", profile: "profile")

#### 属性ハッシュの配列を保存
    user = User.create([{:name => "A"},{:name => "B"}])

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/39c1d2e1840674f2a58dc1ba610fd64a37e950fd/activerecord/lib/active_record/associations/collection_proxy.rb#L289)