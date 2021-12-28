---
layout: page
---

### 説明

型に変更前のハッシュを取得

### 使い方

    モデル.attributes_before_type_cast()

### 例

    task = Task.new(title: nil, is_done: true, completed_on: '2012-10-21')
    task.attributes
    # {"id"=>nil, "title"=>nil, "is_done"=>true, "completed_on"=>Sun, 21 Oct 2012, "created_at"=>nil, "updated_at"=>nil}
    task.attributes_before_type_cast
    # {"id"=>nil, "title"=>nil, "is_done"=>true, "completed_on"=>"2012-10-21", "created_at"=>nil, "updated_at"=>nil}

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/attribute_methods/before_type_cast.rb#L65)
