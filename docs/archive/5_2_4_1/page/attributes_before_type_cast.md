---
layout: archive_page
---
### 説明
型に変更前のハッシュを取得

### 使い方
    モデル.attributes_before_type_cast()

### 例
#### 型に変更前のハッシュを取得
    task = Task.new(title: nil, is_done: true, completed_on: '2012-10-21')
    task.attributes
    # {"id"=>nil, "title"=>nil, "is_done"=>true, "completed_on"=>Sun, 21 Oct 2012, "created_at"=>nil, "updated_at"=>nil}
    task.attributes_before_type_cast
    # {"id"=>nil, "title"=>nil, "is_done"=>true, "completed_on"=>"2012-10-21", "created_at"=>nil, "updated_at"=>nil}

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/attribute_methods/before_type_cast.rb#L62)