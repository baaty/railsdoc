---
layout: page
---
### 説明
データベースから取得したレコードのカラム名を取得する

### 使い方
    モデル.column_for_attribute[:カラム名]

### 例
#### pageのtitleを取得
    @page = Page.find(1)
    @page.column_for_attribute[:title]

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/08576b94ad4f19dfc368619d7751e211d23dcad8/activerecord/lib/active_record/attribute_methods.rb#L206)