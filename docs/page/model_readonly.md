---
layout: page
---

### 説明

読み込み専用としてモデルを取得

### 使い方

    モデル.readonly(値=true)

    # 失敗したら例外発生
    モデル.readonly!(値=true)

### 例

    users = User.readonly
    users.first.save
    # ActiveRecord::ReadOnlyRecord: ActiveRecord::ReadOnlyRecord

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L966)
