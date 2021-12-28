---
layout: page
---

### 説明

条件を指定して初めの1件を取得し1件もなければ作成

### 使い方

    モデル.find_or_create_by(条件, ブロック引数)

    # 失敗したら例外発生
    モデル.find_or_create_by!(条件, ブロック引数)

### 例

#### 存在しないので新しく作成

    User.find_or_create_by(first_name: "Taraou")
    #=> <User id: 1, first_name: "Tarou", last_name: nil>

#### 既に存在する場合は既存のレコードを取得

    User.find_or_create_by(first_name: "Taraou")
    #=> <User id: 1, first_name: "Taraou", last_name: nil>

#### ブロック指定

    User.find_or_create_by(first_name: "Scarlett") do |user|
      user.last_name = "Johansson"
    end
    #=> <User id: 2, first_name: "Scarlett", last_name: "Johansson">

### 補足

- find_or_create_byとの違いは、作成する時に呼ぶメソッドがnewではなくcreate

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation.rb#L168)
