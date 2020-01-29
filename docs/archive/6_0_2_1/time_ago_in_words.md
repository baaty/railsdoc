---
layout: page
---
### 説明
日時を表示
Twitterなどで見かける「3分前」みたいな表示をする場合に使う

### 使い方
    time_ago_in_words(時間 [, オプション])

### 例
    time_ago_in_words(3.minutes.from_now)
    # 3 minutes

    time_ago_in_words(3.minutes.ago)
    # 3 minutes

    time_ago_in_words(Time.now - 15.hours)
    # about 15 hours

    time_ago_in_words(Time.now)
    # less than a minute

    time_ago_in_words(Time.now, include_seconds: true)
    # less than 5 seconds

    from_time = Time.now - 3.days - 14.minutes - 25.seconds
    time_ago_in_words(from_time)
    # 3 days

    from_time = (3.days + 14.minutes + 25.seconds).ago
    time_ago_in_words(from_time)
    # 3 days

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/date_helper.rb#L176)