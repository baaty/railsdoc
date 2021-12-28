---
layout: page
---

### 説明

WHEREと一緒に使用し条件式に一致しないものを取得

### 使い方

    モデル.where.not(条件..)

### 例

#### 条件式に一致しないものを取得

    User.where.not(name: "Jon")
    # SELECT * FROM users WHERE name != 'Jon'

#### nilを指定

    User.where.not(name: nil)
    # SELECT * FROM users WHERE name IS NOT NULL

#### 配列を指定

    User.where.not(name: %w(Ko1 Nobu))
    # SELECT * FROM users WHERE name NOT IN ('Ko1', 'Nobu')

#### 複数条件

    User.where.not(name: "Jon", role: "admin")
    # SELECT * FROM users WHERE name != 'Jon' AND role != 'admin'

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L43)
