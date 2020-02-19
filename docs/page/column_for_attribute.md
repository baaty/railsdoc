---
layout: page
---
### 説明
指定したカラム名のオブジェクトを取得

### 使い方
    モデル.column_for_attribute([カラム名])

### 例
#### pageのtitleを取得
    @page = Page.find(1)
    @page.column_for_attribute(:title)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/attribute_methods.rb#L187)