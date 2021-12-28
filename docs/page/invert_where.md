---
layout: page
---

### 説明

where句全体を反転させて取得

### 使い方

    where句.invert_where()

### 例

#### where句全体を反転させて取得

    User.where(accepted: true)
    # WHERE `accepted` = 1

    User.where(accepted: true).invert_where
    # WHERE `accepted` != 1

#### scopeを指定

    class User
        scope :active, -> { where(accepted: true, locked: false) }
    end

    User.active
    # WHERE `accepted` = 1 AND `locked` = 0

    User.active.invert_where
    # WHERE NOT (`accepted` = 1 AND `locked` = 0)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L776)
