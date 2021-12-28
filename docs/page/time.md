---
layout: page
---

### 説明

時間関係の便利関数

### tomorrow

#### 説明

翌日の時間を取得

#### 使い方

    時間.tomorrow

#### 例

##### 翌日の時間を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).tomorrow
    #  2011-12-25 00:00:00 +0900

#### その他

##### 標準関数で代替

    Time.mktime(2011, 12, 24, 00, 00, 00) + 86400
    #  2011-12-25 00:00:00 +0900

### yesterday

#### 説明

前日の時間を取得

#### 使い方

    時間.yesterday

#### 例

##### 翌日の時間を取得

    Time.mktime(2011, 12, 24).yesterday
    #  2011-12-23 00:00:00 +0900

#### その他

##### 標準関数で代替

    Time.mktime(2011, 12, 24) - 86400
    #  2011-12-23 00:00:00 +0900

### prev_year

#### 説明

去年の時間を取得

#### 使い方

    時間.prev_year

#### 例

##### 去年の時間を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).prev_year
    #  2010-12-24 00:00:00 +0900

#### その他

##### 標準関数で代替

    Time.mktime(2011, 12, 24, 00, 00, 00) - 31536000
    #  2010-12-24 00:00:00 +0900

### next_year

#### 説明

来年の時間を取得

#### 使い方

    時間.next_year

#### 例

##### 来年の時間を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).next_year
    #  2012-12-24 00:00:00 +0900

#### その他

##### 標準関数で代替

    Time.mktime(2011, 12, 24, 00, 00, 00) + 31536000
    #  2012-12-24 00:00:00 +0900

### prev_month

#### 説明

先月の時間を取得

#### 使い方

    時間.prev_month

#### 例

##### 先月の時間を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).prev_month
    # 2011-11-24 00:00:00 +0900

### next_month

#### 説明

来月の時間を取得

#### 使い方

    時間.next_month

#### 例

##### 来月の時間を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).next_month
    # 2012-01-24 00:00:00 +0900

### beginning_of_week

#### 説明

今週の初めの時間を取得

#### 使い方

    時間.beginning_of_week

#### 例

##### 今週の終わりの時間を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).beginning_of_week
    # 2011-12-19 00:00:00 +0900

### end_of_week

#### 説明

今週の終わりの時間を取得

#### 使い方

    時間.end_of_week

#### 例

##### 今週の終わりの時間を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).end_of_week
    # 2011-12-25 23:59:59 +0900

### next_week

#### 説明

来週の時間を取得

#### 使い方

    時間.next_week

#### 例

##### 来週の初めの時間を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).next_week
    # 2011-12-26 00:00:00 +0900

##### 来週の土曜日の時間を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).next_week(:saturday)
    # 2011-12-31 00:00:00 +0900

### prev_week

#### 説明

先週の時間を取得

#### 使い方

    時間.prev_week

#### 例

##### 先週の初めの時間を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).prev_week
    # 2011-12-12 00:00:00 +0900

##### 先週の土曜日の時間を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).prev_week
    # Sat, 17 Dec 2011 00:00:00 +0000

### beginning_of_month

#### 説明

今月の初めの時間を取得

#### 使い方

    時間.beginning_of_month

#### 例

##### 今月の初めの時間を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).beginning_of_month
    # 2011-12-01 00:00:00 +0900

### end_of_month

#### 説明

今月の終わりの時間を取得

#### 使い方

    時間.end_of_month

#### 例

##### 今月の終わりの時間を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).end_of_month
    # 2011-12-31  23:59:59 +0900

### beginning_of_quarter

#### 説明

四半期の初めの時間を取得

#### 使い方

    時間.beginning_of_quarter

#### 例

##### 四半期の初めの時間を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).beginning_of_quarter
    # 2011-10-01 00:00:00 +0900

### end_of_quarter

#### 説明

四半期の終わりの時間を取得

#### 使い方

    時間.end_of_quarter

#### 例

##### 四半期の終わりの時間を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).end_of_quarter
    # 2011-12-31 23:59:59 +0900

### beginning_of_year

#### 説明

今年の初めの時間を取得

#### 使い方

    時間.beginning_of_year

#### 例

##### 今年の初めの時間を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).beginning_of_year
    # 2011-01-01 00:00:00 +0900

### end_of_year

#### 説明

今年の終わりの時間を取得

#### 使い方

    時間.end_of_year

#### 例

##### 今年の終わりの時間を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).end_of_year
    # 2011-12-31 23:59:59 +0900

### years_ago

#### 説明

○年前の時間を取得

#### 使い方

    時間.years_ago(年数)

#### 例

##### 10年前の時間を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).years_ago(10)
    # 2001-12-24 00:00:00 +0900

### years_since

#### 説明

○年後の時間を取得

#### 使い方

    時間.years_since(年数)

#### 例

##### 10年後の時間を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).years_since(10)
    # 2021-12-24 00:00:00 +0900

### months_ago

#### 説明

○月前の時間を取得

#### 使い方

    時間.months_ago(月数)

#### 例

##### 2月前の時間を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).months_ago(2)
    # 2011-10-24 00:00:00 +0900

### months_since

#### 説明

○月後の時間を取得

#### 使い方

    時間.months_since(月数)

#### 例

##### 2月後の時間を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).months_since(2)
    # 2012-02-24 00:00:00 +0900

### weeks_ago

#### 説明

○週前の時間を取得

#### 使い方

    時間.weeks_ago(週数)

#### 例

##### 2週前の時間を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).weeks_ago(2)
    # Sat, 10 Dec 2011 00:00:00 +0000

### advance

#### 説明

特定の時間前の時間を取得

#### 使い方

    時間.advance(時間のハッシュ)

#### 例

##### 2ヶ月後の2日前の時間を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).advance(months: 2, days: -2)
    # 2012-02-22 00:00:00 +0900

### change

#### 説明

特定の時間前の時間を取得

#### 使い方

    時間.change(オプション)

#### オプション

| オプション | 説明 |
| ---------- | ---- |
| :year      | 年   |
| :month     | 月   |
| :day       | 日   |
| :hour      | 時間 |
| :min       | 分   |
| :sec       | 秒   |
| :usec      |      |
| :nsec      |      |
| :offset    |      |

#### 例

##### 2ヶ月後の2日前の時間を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).change(months: 2, days: -2)
    # 2011-12-24 00:00:00 +0900

### 時間の計算

#### 説明

時間を足したり、引いたりする

#### 使い方

    時間 (+ or -) 時間

#### 例

##### 2日後の時間を計算

    Time.mktime(2011, 12, 24, 00, 00, 00) + 2.day
    # 2011-12-26 00:00:00 +0900

##### 1年前の時間を計算

    Time.mktime(2011, 12, 24, 00, 00, 00) - 1.year
    # 2011-12-24 00:00:00 +0900

### beginning_of_day

#### 説明

初めの日時を取得

#### 使い方

    時間.beginning_of_day

#### 例

##### 初めの時刻を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).beginning_of_day

### beginning_of_hour

#### 説明

初めの時刻を取得

#### 使い方

    時間.beginning_of_hour

#### 例

##### 初めの時刻を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).beginning_of_hour

### beginning_of_minute

#### 説明

初めの時刻を取得

#### 使い方

    時間.beginning_of_minute

#### 例

##### 初めの秒数を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).beginning_of_minute

### end_of_day

#### 説明

終わりの日を取得

#### 使い方

    時間.end_of_day

#### 例

##### 今日の1秒後の時刻を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).end_of_day
    # 2011-12-24 23:59:59 +0900

### end_of_hour

#### 説明

終わりの時刻を取得

#### 使い方

    時間.end_of_hour

#### 例

##### 今日の1秒後の時刻を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).end_of_hour

### end_of_minute

#### 説明

終わりの秒数を取得

#### 使い方

    時間.end_of_minute

#### 例

##### 今日の1秒後の時刻を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).end_of_minute

### ago

#### 説明

今日の○秒前の時刻を取得

#### 使い方

    時間.ago(秒数)

#### 例

##### 今日の1秒前の時刻を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).ago(1)
    # 2011-12-23 23:59:59 +0900

### since

#### 説明

今日の○秒後の時刻を取得

#### 使い方

    時間.since(秒数)

#### 例

##### 今日の1秒後の時刻を取得

    Time.mktime(2011, 12, 24, 00, 00, 00).since(1)
    # 2011-12-24 00:00:01 +0900

### seconds_since_midnight

#### 説明

今日の0時からの秒数を取得

#### 使い方

    時間.seconds_since_midnight

#### 例

##### 今日の0時からの秒数を取得

    Time.mktime(2011, 12, 24, 10, 00, 00).seconds_since_midnight
    # 36000.0

### utc

#### 説明

UTCの時間を取得

#### 使い方

    時間.seconds_since_midnight

#### 例

##### UTCの時間を取得

    Time.current.utc # 2011-12-24 00:00:00 +0900
    # 2011-12-23 15:00:00 UTC

### zone_default

#### 説明

UTCの時間を取得

#### 使い方

    時間.zone_default

#### 例

##### UTCの時間を取得

    Time.zone_default
    # (GMT+09:00) Tokyo

### days_in_month

#### 説明

月の日数を取得

#### 使い方

    Time.days_in_month(月 [, 年])

#### 例

##### 2020年2月の日数

    Time.days_in_month(2, 2020)
    # 29

##### 今年の2月の日数

    Time.days_in_month(2)
    # 29

### days_in_year

#### 説明

年の日数を取得

#### 使い方

    Time.days_in_year(月 [, 年])

#### 例

##### 2020年の日数

    Time.days_in_year(2, 2020)
    # 365

##### 今年の日数

    Time.days_in_year(2)
    # 365

### find_zone

#### 説明

指定したタイムゾーンを取得

#### 使い方

    Time.find_zone(タイムゾーン)

#### 例

    Time.find_zone "Tokyo"

### rfc3339

#### 説明

RFC3339文字列からTimeを生成

#### 使い方

    Time.rfc3339(文字列)

#### 例

    Time.rfc3339('1999-12-31T14:00:00-10:00')
    # 2000-01-01 00:00:00 -1000

### use_zone

#### 説明

一時的にタイムゾーンを変更

#### 使い方

    Time.use_zone(文字列) {
        処理内容
    }

#### 例

    Time.use_zone "Tokyo" {
        Time.local(2019, 01, 01, 00, 00, 00)
    }

### formatted_offset

#### 説明

オフセットのフォーマット

#### 使い方

    Time.now.formatted_offset([コロンの有無])

#### 例

    Time.local(2000).formatted_offset
    # "-06:00"

    Time.local(2000).formatted_offset(false)
    # "-0600"

### middle_of_day

#### 説明

日中(12:00)

#### 使い方

    Time.now.middle_of_day

#### 例

    Time.mktime(2011, 12, 24, 00, 00, 00).middle_of_day

### next_day

#### 説明

指定した日の次の日

#### 使い方

    Time.now.next_day

#### 例

    Time.mktime(2011, 12, 24, 00, 00, 00).next_day

### next_month

#### 説明

指定した日の次の月

#### 使い方

    Time.next_month

#### 例

    Time.mktime(2011, 12, 24, 00, 00, 00).next_month

### next_year

#### 説明

指定した日の次の年

#### 使い方

    Time.now.next_year

#### 例

    Time.mktime(2011, 12, 24, 00, 00, 00).next_year

### prev_day

#### 説明

指定した日の前の日

#### 使い方

    Time.prev_day

#### 例

    Time.mktime(2011, 12, 24, 00, 00, 00).prev_day

### prev_month

#### 説明

指定した日の前の月

#### 使い方

    Time.now.prev_month

#### 例

    Time.mktime(2011, 12, 24, 00, 00, 00).prev_month

### prev_year

#### 説明

指定した日の前の年

#### 使い方

    Time.prev_year

#### 例

    Time.mktime(2011, 12, 24, 00, 00, 00).prev_year

### seconds_since_midnight

#### 説明

00:00:00からの秒数

#### 使い方

    Time.now.seconds_since_midnight

#### 例

    Time.mktime(2011, 12, 24, 00, 00, 00).seconds_since_midnight

### seconds_until_end_of_day

#### 説明

23:59:59までの秒数

#### 使い方

    Time.now.seconds_until_end_of_day

#### 例

    Time.mktime(2011, 12, 24, 00, 00, 00).seconds_until_end_of_day

### to_formatted_s

#### 説明

指定したフォーマットに変換

#### 使い方

    Time.now.to_formatted_s(フォーマット)

#### 例

    Time.now.to_formatted_s(:time)
    # "06:10"

    Time.now.to_s(:time)
    # "06:10"

    Time.now.to_formatted_s(:db)
    # "2007-01-18 06:10:17"

    Time.now.to_formatted_s(:number)
    # "20070118061017"

    Time.now.to_formatted_s(:short)
    # "18 Jan 06:10"

    Time.now.to_formatted_s(:long)
    # "January 18, 2007 06:10"

    Time.now.to_formatted_s(:long_ordinal)
    # "January 18th, 2007 06:10"

    Time.now.to_formatted_s(:rfc822)
    # "Thu, 18 Jan 2007 06:10:17 -0600"

    Time.now.to_formatted_s(:iso8601)
    # "2007-01-18T06:10:17-06:00"
