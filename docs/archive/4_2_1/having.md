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
* [GitHub](https://github.com/rails/rails/blob/0399b71dab8b270b4e40b2aff99194a8b8f2596c/activerecord/lib/active_record/relation/query_methods.rb#L604)