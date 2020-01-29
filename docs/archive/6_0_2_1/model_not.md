---
layout: page
---
### 説明
WHEREと一緒に使用し、条件式に一致しないものを取得

### 使い方
    モデル.where.not(条件)

### 例
    User.where.not("name = 'Jon'")
    # SELECT * FROM users WHERE NOT (name = 'Jon')

    User.where.not(["name = ?", "Jon"])
    # SELECT * FROM users WHERE NOT (name = 'Jon')

    User.where.not(name: "Jon")
    # SELECT * FROM users WHERE name != 'Jon'

    User.where.not(name: nil)
    # SELECT * FROM users WHERE name IS NOT NULL

    User.where.not(name: %w(Ko1 Nobu))
    # SELECT * FROM users WHERE name NOT IN ('Ko1', 'Nobu')

    User.where.not(name: "Jon", role: "admin")
    # SELECT * FROM users WHERE name != 'Jon' AND role != 'admin'

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/query_methods.rb#L44)