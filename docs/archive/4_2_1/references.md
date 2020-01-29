---
layout: page
---
### 説明
他のテーブルへの外部キーを表すカラムを生成

### 使い方
    references

### 例
#### belongs_to :user_idと同じ
    create_table :blogs do |t|
    &nbsp;&nbsp;t.references("user")
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0230ad686118b60e89ef8cd2f7b2936099de6deb/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L550)