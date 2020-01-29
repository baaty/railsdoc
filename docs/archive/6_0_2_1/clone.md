---
layout: page
---
### 説明
モデルのコピーを生成

### 使い方
    モデル.clone

### 例
    user = User.first
    new_user = user.clone
    user.name               # "Bob"
    new_user.name = "Joe"
    user.name               # "Joe"

    user.object_id == new_user.object_id            # false
    user.name.object_id == new_user.name.object_id  # true

    user.name.object_id == user.dup.name.object_id  # false

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/core.rb#L387)