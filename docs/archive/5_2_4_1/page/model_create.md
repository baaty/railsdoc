---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/persistence.rb#L31)