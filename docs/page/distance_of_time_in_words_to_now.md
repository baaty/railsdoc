---
layout: page
---

### 説明

現在までのおおよその経過時間

### 使い方

    distance_of_time_in_words_to_now(開始時間, オプション={})

### 例

    from_time = Time.now
    distance_of_time_in_words_to_now(from_time + 50.minutes)
    #=> about 1 hour

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/date_helper.rb#L176)
