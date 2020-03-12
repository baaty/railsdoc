---
layout: archive_page
---
### 説明
関連するテーブルをまとめて取得

### 使い方
    モデル.includes(:モデル [, ...])

### 例
#### 基本的な使い方
    Page.includes(:category)
    # SELECT "pages".* FROM "pages"
    # SELECT "categories".* FROM "categories" WHERE "categories"."id" IN (1)

#### 複数指定
    User.includes(:address, :friends)

#### 孫モデルをまとめる
    User.includes(friends: :address)

#### 子モデルが存在するレコードを取得
    User.joins(:friends).where("friends.id IS NOT NULL")

#### 孫モデルが存在するレコードを取得
    User.friends.joins(:followers).where("followers.id IS NOT NULL")

#### OR演算子を指定
    User.where(address: 'hoge').or(User.where(friends: 'fuga'))

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/query_methods.rb#L114)