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
* [GitHub](https://github.com/rails/rails/blob/0399b71dab8b270b4e40b2aff99194a8b8f2596c/activerecord/lib/active_record/relation/query_methods.rb#L41)