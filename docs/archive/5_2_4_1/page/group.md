---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/query_methods.rb#L259)