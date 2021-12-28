---
layout: page
---

### 説明

取得した値をグループ化

### 使い方

    モデル.group(グループ化キー..)

### 例

#### usersテーブルをnameでグルーピング

    User.group("name")
    # SELECT * FROM users GROUP BY name

#### 複数指定

    User.group('name, age')
    # SELECT * FROM users GROUP BY name, age

#### 年齢ごとの件数

    User.group(:age).count

#### 結合してグルーピング

    User.joins(:categories).group("categories.name")

#### 3つのテーブル

    User.joins(categories: :tags).group("user.name")

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L347)
