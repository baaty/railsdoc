---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/persistence.rb#L651)