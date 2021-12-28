---
layout: page
---

### 説明

2つの時間のおおよその経過時間

### 使い方

    distance_of_time_in_words(開始時間, 終了時間=0, オプション={})

### 例

    from_time = Time.now
    distance_of_time_in_words(from_time, from_time + 50.minutes)                                #=> about 1 hour
    distance_of_time_in_words(from_time, 50.minutes.from_now)                                   #=> about 1 hour
    distance_of_time_in_words(from_time, from_time + 15.seconds)                                #=> less than a minute
    distance_of_time_in_words(from_time, from_time + 15.seconds, include_seconds: true)         #=> less than 20 seconds
    distance_of_time_in_words(from_time, 3.years.from_now)                                      #=> about 3 years
    distance_of_time_in_words(from_time, from_time + 60.hours)                                  #=> 3 days
    distance_of_time_in_words(from_time, from_time + 45.seconds, include_seconds: true)         #=> less than a minute
    distance_of_time_in_words(from_time, from_time - 45.seconds, include_seconds: true)         #=> less than a minute
    distance_of_time_in_words(from_time, 76.seconds.from_now)                                   #=> 1 minute
    distance_of_time_in_words(from_time, from_time + 1.year + 3.days)                           #=> about 1 year
    distance_of_time_in_words(from_time, from_time + 3.years + 6.months)                        #=> over 3 years
    distance_of_time_in_words(from_time, from_time + 4.years + 9.days + 30.minutes + 5.seconds) #=> about 4 years

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/date_helper.rb#L176)
