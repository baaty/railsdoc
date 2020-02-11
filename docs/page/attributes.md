---
layout: page
---
### 説明
全てのモデルオブジェクトと属性を取得

### 使い方
    モデル.attributes()

### 例
#### 全てのモデルオブジェクトと属性を取得
    person = Person.create(name: 'Francesco', age: 22)
    person.attributes
    # {"id"=>3, "created_at"=>Sun, 21 Oct 2012 04:53:04, "updated_at"=>Sun, 21 Oct 2012 04:53:04, "name"=>"Francesco", "age"=>22}

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/attribute_methods.rb#L260)