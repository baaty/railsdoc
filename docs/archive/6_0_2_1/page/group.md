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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/query_methods.rb#L326)