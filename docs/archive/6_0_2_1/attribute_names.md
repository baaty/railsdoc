---
layout: page
---
### 説明
テーブルのすべてのカラム名を取得

### 使い方
    モデル.attribute_names

### 例
#### pagesテーブルのすべてのカラム名を取得
    Person.attribute_names
    # ["id", "created_at", "updated_at", "name", "age"]

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/attribute_methods.rb#L154)