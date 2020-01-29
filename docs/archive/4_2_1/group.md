---
layout: page
---
### 説明
取得した値をグループ化

### 使い方
    モデル.group(グループ化キー)

### 例
#### usersテーブルをnameでグルーピング
    User.group("name")
    # SELECT * FROM users GROUP BY name

    User.group('name, age')
    # SELECT * FROM users GROUP BY name, age

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0399b71dab8b270b4e40b2aff99194a8b8f2596c/activerecord/lib/active_record/relation/query_methods.rb#L286)