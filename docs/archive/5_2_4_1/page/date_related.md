---
layout: archive_page
---
### tomorrow
#### 説明
翌日の日付を取得

#### 使い方
    日付.tomorrow

#### 例
##### 翌日の日付を取得
    Date.new(2011, 12, 24).tomorrow
    #  Sun, 25 Dec 2011

#### その他
##### 標準関数で代替
    Date.new(2011, 12, 24) + 1
    #  Sun, 25 Dec 2011

### yesterday
#### 説明
前日の日付を取得

#### 使い方
    日付.yesterday

#### 例
##### 翌日の日付を取得
    Date.new(2011, 12, 24).yesterday
    #  Fri, 23 Dec 2011

#### その他
##### 標準関数で代替
    Date.new(2011, 12, 24) - 1
    #  Fri, 23 Dec 2012

### prev_year
#### 説明
前の年の日付を取得

#### 使い方
    日付.prev_year

#### 例
##### 去年の日付を取得
    Date.new(2011, 12, 24).prev_year
    #  Fri, 24 Dec 2010

#### その他
##### 標準関数で代替
    Date.new(2011, 12, 24) << 12
    #  Fri, 24 Dec 2010

### next_year
#### 説明
次の年の日付を取得

#### 使い方
    日付.next_year

#### 例
##### 来年の日付を取得
    Date.new(2011, 12, 24).next_year
    #  Mon, 24 Dec 2012

#### その他
##### 標準関数で代替
    Date.new(2011, 12, 24) >> 12
    #  Mon, 24 Dec 2012

### prev_month
#### 説明
前の月の日付を取得

#### 使い方
    日付.prev_month

#### 例
##### 先月の日付を取得
    Date.new(2011, 12, 24).prev_month
    # Thu,  24 Nov 2011

#### その他
##### 標準関数で代替
    Date.new(2011, 12, 24) << 1
    # Thu, 24 Nov 2011

### next_month
#### 説明
次の月の日付を取得

#### 使い方
    日付.next_month

#### 例
##### 来月の日付を取得
    Date.new(2011, 12, 24).next_month
    # Tue,  24 Jan 2012

#### その他
##### 標準関数で代替
    Date.new(2011, 12, 24) >> 1
    #  Tue, 24 Jan 2012

### beginning_of_week
#### 説明
週の初めの日付を取得

#### 使い方
    日付.beginning_of_week

#### 例
##### 今週の終わりの日付を取得
    Date.new(2011, 12, 24).beginning_of_week
    # Mon, 19 Dec 2011

### end_of_week
#### 説明
週の終わりの日付を取得

#### 使い方
    日付.end_of_week

#### 例
##### 今週の終わりの日付を取得
    Date.new(2011, 12, 24).end_of_week
    # Sun, 25 Dec 2011

### next_week
#### 説明
来週の日付を取得

#### 使い方
    日付.next_week

#### 例
##### 来週の初めの日付を取得
    Date.new(2011, 12, 24).next_week
    # Mon, 26 Dec 2011

##### 来週の土曜日の日付を取得
    Date.new(2011, 12, 24).next_week(:saturday)
    # Sat, 31 Dec 2011

### prev_week
#### 説明
先週の日付を取得

#### 使い方
    日付.prev_week

#### 例
##### 先週の初めの日付を取得
    Date.new(2011, 12, 24).prev_week
    # Mon, 12 Dec 2011

##### 先週の土曜日の日付を取得
    Date.new(2011, 12, 24).prev_week
    # Sat, 17 Dec 2011

### beginning_of_month
#### 説明
月の初めの日付を取得

#### 使い方
    日付.beginning_of_month

#### 例
##### 今月の初めの日付を取得
    Date.new(2011, 12, 24).beginning_of_month
    # Thu, 01 Dec 2011

### end_of_month
#### 説明
月の終わりの日付を取得

#### 使い方
    日付.end_of_month

#### 例
##### 今月の終わりの日付を取得
    Date.new(2011, 12, 24).end_of_month
    # Sat, 31 Dec 2011

### beginning_of_quarter
#### 説明
四半期の初めの日付を取得

#### 使い方
    日付.beginning_of_quarter

#### 例
##### 四半期の初めの日付を取得
    Date.new(2011, 12, 24).beginning_of_quarter
    # Sat, 01 Oct 2011

### end_of_quarter
#### 説明
四半期の終わりの日付を取得

#### 使い方
    日付.end_of_quarter

#### 例
##### 四半期の終わりの日付を取得
    Date.new(2011, 12, 24).end_of_quarter
    # Sat, 31 Dec 2011

### beginning_of_year
#### 説明
年の初めの日付を取得

#### 使い方
    日付.beginning_of_year

#### 例
##### 今年の初めの日付を取得
    Date.new(2011, 12, 24).beginning_of_year
    # Sat, 01 Jan 2011

### end_of_year
#### 説明
年の終わりの日付を取得

#### 使い方
    日付.end_of_year

#### 例
##### 今年の終わりの日付を取得
    Date.new(2011, 12, 24).end_of_year
    # Sat, 31 Dec 2011

### years_ago
#### 説明
○年前の日付を取得

#### 使い方
    日付.years_ago(年数)

#### 例
##### 10年前の日付を取得
    Date.new(2011, 12, 24).years_ago(10)
    # Mon, 24 Dec 2001

### years_ago
#### 説明
○年前の日付を取得

#### 使い方
    日付.years_ago(年数)

#### 例
##### 10年前の日付を取得
    Date.new(2011, 12, 24).years_ago(10)
    # Mon, 24 Dec 2001

### years_since
#### 説明
○年後の日付を取得

#### 使い方
    日付.years_since(年数)

#### 例
##### 10年後の日付を取得
    Date.new(2011, 12, 24).years_since(10)
    # Fri, 24 Dec 2021

### months_ago
#### 説明
○月前の日付を取得

#### 使い方
    日付.months_ago(月数)

#### 例
##### 2月前の日付を取得
    Date.new(2011, 12, 24).months_ago(2)
    # Mon, 24 Oct 2011

### months_since
#### 説明
○月後の日付を取得

#### 使い方
    日付.months_since(月数)

#### 例
##### 2月後の日付を取得
    Date.new(2011, 12, 24).months_since(2)
    # Fri, 24 Feb 2012

### weeks_ago
#### 説明
○週前の日付を取得

#### 使い方
    日付.weeks_ago(週数)

#### 例
##### 2週前の日付を取得
    Date.new(2011, 12, 24).weeks_ago(2)
    # Sat, 10 Dec 2011

### advance
#### 説明
特定の日時前の日付を取得

#### 使い方
    日付.advance(日付のハッシュ)

#### 例
##### 2ヶ月後の2日前の日付を取得
    Date.new(2011, 12, 24).advance(months: 2, days: -2)
    # Wed, 22 Feb 2011

### change
#### 説明
特定の日時前の日付を取得

#### 使い方
    日付.change(日付のハッシュ)

#### 例
##### 2ヶ月後の2日前の日付を取得
    Date.new(2011, 12, 24).change(months: 2, days: -2)
    # Sat, 24 Dec 2011

### 日付の計算
#### 説明
日付を足したり、引いたりする

#### 使い方
    日付 (+ or -) 日付

#### 例
##### 2日後の日付を計算
    Date.new(2011, 12, 24) + 2.day
    # Mon, 26 Dec 2011

##### 1年前の日付を計算
    Date.new(2011, 12, 24) - 1.year
    # Fri, 24 Dec 2010

### beginning_of_day
#### 説明
初めの時刻を取得

#### 使い方
    日付.beginning_of_day

#### 例
##### 今日の初めの時刻を取得
    Date.new(2011, 12, 24).beginning_of_day
    # Sat, 24 Dec 2011 00:00:00 JST +09:00


### beginning_of_hour
#### 説明
初めの分を取得

#### 使い方
    日付.beginning_of_hour

#### 例
##### 今日の初めの時刻を取得
    Date.new(2011, 12, 24, 10, 55, 55).beginning_of_hour
    # Sat, 24 Dec 2011 10:00:00 JST +09:00

### end_of_day
#### 説明
終わりの時刻を取得

#### 使い方
    日付.end_of_day

#### 例
##### 今日の1秒後の時刻を取得
    Date.new(2011, 12, 24).end_of_day
    # Sat, 24 Dec 2011 23:59:59 JST +09:00

### ago
#### 説明
○秒前の時刻を取得

#### 使い方
    日付.ago(秒数)

#### 例
##### 今日の1秒前の時刻を取得
    Date.new(2011, 12, 24).ago(1)
    # Sat, 23 Dec 2011 23:59:59 JST +09:00

### since
#### 説明
○秒後の時刻を取得

#### 使い方
    日付.since(秒数)

#### 例
##### 今日の1秒後の時刻を取得
    Date.new(2011, 12, 24).since(1)
    # Sat, 24 Dec 2011 00:00:01 JST +09:00