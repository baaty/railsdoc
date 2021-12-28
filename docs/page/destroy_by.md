---
layout: page
---

### 説明

指定された条件に一致するレコードと関連するレコードを検索してすべて削除

### 使い方

    モデル.destroy_by(条件..)

### 例

    Person.destroy_by(id: 13)
    Person.destroy_by(name: 'Spartacus', rating: 4)
    Person.destroy_by("published_at < ?", 2.weeks.ago)

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation.rb#L642)
