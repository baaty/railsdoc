---
layout: archive_page
---
### 説明
WHEREと一緒に使用し、条件式に一致しないものを取得

### 使い方
    モデル.where.not(条件)

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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/query_methods.rb#L47)