---
layout: page
---

### 説明

日時を表示  
Twitterなどで見かける「3分前」みたいな表示をする場合に使う

### 使い方

    time_ago_in_words(時間, オプション={})

### 例

#### 日時を表示

    time_ago_in_words(3.minutes.from_now)
    # 3 minutes

#### 3分

    time_ago_in_words(3.minutes.ago)
    # 3 minutes

#### 約15時間

    time_ago_in_words(Time.now - 15.hours)
    # about 15 hours

#### 1分未満

    time_ago_in_words(Time.now)
    # less than a minute

#### より詳しい時間を取得

    time_ago_in_words(Time.now, include_seconds: true)
    # less than 5 seconds

#### 変数を指定

    from_time = Time.now - 3.days - 14.minutes - 25.seconds
    time_ago_in_words(from_time)
    # 3 days

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/date_helper.rb#L176)
