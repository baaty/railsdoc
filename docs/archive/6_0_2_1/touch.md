---
layout: page
---
### 説明
update_atを現在の時刻でアップデートする。検証やコールバックを実施されない

### 使い方
    モデル.touch([名前])

### 例
    product.touch
    # updates updated_at/on with current time

    product.touch(time: Time.new(2015, 2, 16, 0, 0, 0))
    # updates updated_at/on with specified time

    product.touch(:designed_at)
    # updates the designed_at attribute and updated_at/on

    product.touch(:started_at, :ended_at)
    # updates started_at, ended_at and updated_at/on attributes

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/persistence.rb#L851)