---
layout: page
---

### 説明

指定した条件に一致するレコードをSQLを直接実行して全て削除  
関連付けられたモデルは削除しない

### 使い方

    モデル.delete_all()

### 例

    Post.where(person_id: 5).where(category: ['Something', 'Else']).delete_all

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation.rb#L601)
