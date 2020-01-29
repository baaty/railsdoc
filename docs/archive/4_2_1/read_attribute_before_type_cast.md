---
layout: page
---
### 説明
型に変更前のハッシュを取得

### 使い方
    モデル.read_attribute_before_type_cast(カラム名)

### 例
    task = Task.new(id: '1', completed_on: '2012-10-21')
    task.read_attribute('id')                            # => 1
    task.read_attribute_before_type_cast('id')           # => '1'
    task.read_attribute('completed_on')                  # => Sun, 21 Oct 2012
    task.read_attribute_before_type_cast('completed_on') # => "2012-10-21"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/3e74db6361cf61434fa47f44fcbccf50ce02bad8/activerecord/lib/active_record/attribute_methods/before_type_cast.rb#L46)