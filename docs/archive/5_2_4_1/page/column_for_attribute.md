---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/attribute_methods.rb#L246)