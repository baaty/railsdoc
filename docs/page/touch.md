---
layout: page
---

### 説明

update_atを現在の時刻でアップデート  
バリデーションやコールバックを実施されない

### 使い方

    モデル.touch([名前])

### 例

#### update_atを現在の時刻でアップデート

    product.touch

#### update_atを指定した時刻でアップデート

    product.touch(time: Time.new(2015, 2, 16, 0, 0, 0))
    # updates updated_at/on with specified time

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/persistence.rb#L993)
