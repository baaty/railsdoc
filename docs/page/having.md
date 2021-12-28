---
layout: page
---

### 説明

モデルから取得した値を元に絞り込む

### 使い方

    モデル.having(条件式)

### 例

#### 絞り込む

    User.having(['AVG(age) >= ?', 30])
    # SELECT * FROM users HAVING AVG(age) >= 30

#### グループ後に絞り込む

    User.select('age, count(*) as count').group('age').having('count >= ?', 30)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L868)
