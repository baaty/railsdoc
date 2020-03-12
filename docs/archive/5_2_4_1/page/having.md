---
layout: archive_page
---
### 説明
モデルから取得した値を元に絞り込む

### 使い方
    モデル.having(条件式)

### 例
#### 平均ageが30以上を取得
    User.having(['AVG(age) >= ?', 30])
    # SELECT * FROM users HAVING AVG(age) >= 30

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/query_methods.rb#L645)