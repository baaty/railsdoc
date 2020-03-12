---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/attribute_methods.rb#L326)