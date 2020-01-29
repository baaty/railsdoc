---
layout: page
---
### 説明
重複のないレコードを取得

### 使い方
    モデル.uniq(値)

### 例
    User.select(:name)
    # => Might return two records with the same name

    User.select(:name).uniq
    # => Returns 1 record per unique name

    User.select(:name).uniq.uniq(false)
    # => You can also remove the uniqueness