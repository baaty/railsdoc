---
layout: page
---
### 説明
検索条件を指定して初めの1件を取得し、1件もなければ作成

### 使い方
    モデル.find_or_create_by(条件)

### 例
    # Find the first user named Penélope or create a new one.
    User.find_or_create_by(first_name: 'Penélope')
    # => <User id: 1, first_name: 'Penélope', last_name: nil>

    # Find the first user named Penélope or create a new one.
    # We already have one so the existing record will be returned.
    User.find_or_create_by(first_name: 'Penélope')
    # => <User id: 1, first_name: 'Penélope', last_name: nil>

    # Find the first user named Scarlett or create a new one with a particular last name.
    User.create_with(last_name: 'Johansson').find_or_create_by(first_name: 'Scarlett')
    # => <User id: 2, first_name: 'Scarlett', last_name: 'Johansson'>

    # Find the first user named Scarlett or create a new one with a different last name.
    # We already have one so the existing record will be returned.
    User.find_or_create_by(first_name: 'Scarlett') do |user|
      user.last_name = "O'Hara"
    end
    # => <User id: 2, first_name: 'Scarlett', last_name: 'Johansson'>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/78bd18a90992e3da767cfe492f1bc5d63077da8a/activerecord/lib/active_record/relation.rb#L211)