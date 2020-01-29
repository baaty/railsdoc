---
layout: page
---
### 説明
モデルの全てのカラムと属性を取得する

### 使い方
    モデル.attributes

### 例
#### pageのtitleを取得
    @page = Page.find(1)
    @page.attributes

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/08576b94ad4f19dfc368619d7751e211d23dcad8/activerecord/lib/active_record/attribute_methods.rb#L283)