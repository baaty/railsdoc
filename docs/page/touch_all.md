---
layout: page
---

### 説明

updated_atとupdated_on属性を現在の時刻または指定された時刻に設定

### 使い方

    モデル.touch_all(時刻のカラム名.., time: 時間=nil)

### 例

#### 現在時刻に設定

    Person.all.touch_all
    # "UPDATE \"people\" SET \"updated_at\" = '2018-01-04 22:55:23.132670'"

#### 時刻のカラム名を指定

    Person.all.touch_all(:created_at)
    # "UPDATE \"people\" SET \"updated_at\" = '2018-01-04 22:55:23.132670', \"created_at\" = '2018-01-04 22:55:23.132670'"

#### 時間を指定

    Person.all.touch_all(time: Time.new(2020, 5, 16, 0, 0, 0))
    # "UPDATE \"people\" SET \"updated_at\" = '2020-05-16 00:00:00'"

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation.rb#L559)
