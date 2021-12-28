---
layout: page
---

### 説明

属性に反対のブール値を割り当てる

### 使い方

    モデル.toggle(属性)

    # 失敗したら例外発生
    モデル.toggle!(属性)

### 例

    user = User.first
    user.banned? #=> false
    user.toggle(:banned)
    user.banned? #=> true

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/persistence.rb#L882)
