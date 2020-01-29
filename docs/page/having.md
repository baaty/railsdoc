---
layout: page
---
### 説明
データベースから取得した値を元に絞り込む

### 使い方
    モデル.having(条件式)

### 例
#### 平均ageが30以上を取得
    User.having(['AVG(age) >= ?', 30])
    # SELECT * FROM users HAVING AVG(age) >= 30

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/query_methods.rb#L713)