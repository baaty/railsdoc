---
layout: archive_page
---
### 説明
モデルのコピーを生成

### 使い方
    モデル.clone()

### 例
#### モデルのコピーを生成
    user = User.first
    new_user = user.clone
    user.name               # "Bob"
    new_user.name = "Joe"
    user.name               # "Joe"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/core.rb#L370)