---
layout: page
---
### 説明
日時関連の便利関数

### tomorrow
#### 説明
翌日の日時を取得

#### 使い方
    <日時>.tomorrow

#### 例
##### 翌日の日時を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).tomorrow
    #  Sun, 25 Dec 2011 00:00:00 +0000

#### その他
##### 標準関数で代替
    DateTime.new(2011, 12, 24, 00, 00, 00) + 1
    #  Sun, 25 Dec 2011 00:00:00 +0000

### yesterday
#### 説明
前日の日時を取得

#### 使い方
    <日時>.yesterday

#### 例
##### 前日の日時を取得
    DateTime.new(2011, 12, 24).yesterday
    #  Fri, 23 Dec 2011 00:00:00 +0000

#### その他
##### 標準関数で代替
    DateTime.new(2011, 12, 24) - 1
    #  Fri, 23 Dec 2011 00:00:00 +0000

### prev_year
#### 説明
去年の日時を取得

#### 使い方
    <日時>.prev_year

#### 例
##### 去年の日時を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).prev_year
    #  Fri, 24 Dec 2010 00:00:00 +0000

#### その他
##### 標準関数で代替
    DateTime.new(2011, 12, 24, 00, 00, 00) << 12
    #  Fri, 24 Dec 2010 00:00:00 +0000

### next_year
#### 説明
来年の日時を取得

#### 使い方
    <日時>.next_year

#### 例
##### 来年の日時を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).next_year
    #  Mon, 24 Dec 2012 00:00:00 +0000

#### その他
##### 標準関数で代替
    DateTime.new(2011, 12, 24, 00, 00, 00) >> 12
    #  Mon, 24 Dec 2012 00:00:00 +0000

### prev_month
#### 説明
先月の日時を取得

#### 使い方
    <日時>.prev_month

#### 例
##### 先月の日時を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).prev_month
    # Thu,  24 Nov 2011 00:00:00 +0000

#### その他
##### 標準関数で代替
    DateTime.new(2011, 12, 24, 00, 00, 00) << 1
    # Thu,  24 Nov 2011 00:00:00 +0000

### next_month
#### 説明
来月の日時を取得

#### 使い方
    <日時>.next_month

#### 例
##### 来月の日時を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).next_month
    # Tue,  24 Jan 2012 00:00:00 +0000

#### その他
##### 標準関数で代替
    DateTime.new(2011, 12, 24, 00, 00, 00) >> 1
    # Tue,  24 Jan 2012 00:00:00 +0000

### beginning_of_week
#### 説明
今週の初めの日時を取得

#### 使い方
    <日時>.beginning_of_week

#### 例
##### 今週の終わりの日時を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).beginning_of_week
    # Mon, 19 Dec 2011 00:00:00 +0000

### end_of_week
#### 説明
今週の終わりの日時を取得

#### 使い方
    <日時>.end_of_week

#### 例
##### 今週の終わりの日時を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).end_of_week
    # Sun, 25 Dec 2011 23:59:59 +0000

### next_week
#### 説明
来週の日時を取得

#### 使い方
    <日時>.next_week

#### 例
##### 来週の初めの日時を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).next_week
    # Mon, 26 Dec 2011 00:00:00 +0000

##### 来週の土曜日の日時を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).next_week(:saturday)
    # Sat, 31 Dec 2011 00:00:00 +0000

### prev_week
#### 説明
先週の日時を取得

#### 使い方
    <日時>.prev_week

#### 例
##### 先週の初めの日時を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).prev_week
    # Mon, 12 Dec 2011 00:00:00 +0000

##### 先週の土曜日の日時を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).prev_week
    # Sat, 17 Dec 2011 00:00:00 +0000

### beginning_of_month
#### 説明
今月の初めの日時を取得

#### 使い方
    <日時>.beginning_of_month

#### 例
##### 今月の初めの日時を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).beginning_of_month
    # Thu, 01 Dec 2011 00:00:00 +0000

### end_of_month
#### 説明
今月の終わりの日時を取得

#### 使い方
    <日時>.end_of_month

#### 例
##### 今月の終わりの日時を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).end_of_month
    # Sat, 31 Dec 2011 23:59:59 +0000

### beginning_of_quarter
#### 説明
四半期の初めの日時を取得

#### 使い方
    <日時>.beginning_of_quarter

#### 例
##### 四半期の初めの日時を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).beginning_of_quarter
    # Sat, 01 Oct 2011 00:00:00 +0000

### end_of_quarter
#### 説明
四半期の終わりの日時を取得

#### 使い方
    <日時>.end_of_quarter

#### 例
##### 四半期の終わりの日時を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).end_of_quarter
    # Sat, 31 Dec 2011 23:59:59 +0000

### beginning_of_year
#### 説明
今年の初めの日時を取得

#### 使い方
    <日時>.beginning_of_year

#### 例
##### 今年の初めの日時を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).beginning_of_year
    # Sat, 01 Jan 2011 00:00:00 +0000

### end_of_year
#### 説明
今年の終わりの日時を取得

#### 使い方
    <日時>.end_of_year

#### 例
##### 今年の終わりの日時を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).end_of_year
    # Sat, 31 Dec 2011 23:59:59 +0000

### years_ago
#### 説明
○年前の日時を取得

#### 使い方
    <日時>.years_ago(<年数>)

#### 例
##### 10年前の日時を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).years_ago(10)
    # Mon, 24 Dec 2001 00:00:00 +0000

### years_since
#### 説明
○年後の日時を取得

#### 使い方
    <日時>.years_since(<年数>)

#### 例
##### 10年後の日時を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).years_since(10)
    # Fri, 24 Dec 2021 00:00:00 +0000

### months_ago
#### 説明
○月前の日時を取得

#### 使い方
    <日時>.months_ago(<月数>)

#### 例
##### 2月前の日時を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).months_ago(2)
    # Mon, 24 Oct 2011 00:00:00 +0000

### months_since
#### 説明
○月後の日時を取得

#### 使い方
    <日時>.months_since(<月数>)

#### 例
##### 2月後の日時を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).months_since(2)
    # Fri, 24 Feb 2012 00:00:00 +0000

### weeks_ago
#### 説明
○週前の日時を取得

#### 使い方
    <日時>.weeks_ago(<週数>)

#### 例
##### 2週前の日時を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).weeks_ago(2)
    # Sat, 10 Dec 2011 00:00:00 +0000

### advance
#### 説明
特定の日時前の日時を取得

#### 使い方
    <日時>.advance(<日時のハッシュ>)

#### 例
##### 2ヶ月後の2日前の日時を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).advance(:months => 2, :days => -2)
    # Wed, 22 Feb 2011 00:00:00 +0000

### change
#### 説明
特定の日時前の日時を取得

#### 使い方
    <日時>.change(<日時のハッシュ>)

#### 例
##### 2ヶ月後の2日前の日時を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).change(:months => 2, :days => -2)
    # Sat, 24 Dec 2011 00:00:00 +0000

### 日時の計算
#### 説明
日時を足したり、引いたりする

#### 使い方
    <日時> (+ or -) <日時>

#### 例
##### 2日後の日時を計算
    DateTime.new(2011, 12, 24, 00, 00, 00) + 2.day
    # Mon, 26 Dec 2011 00:00:00 +0000

##### 1年前の日時を計算
    DateTime.new(2011, 12, 24, 00, 00, 00) - 1.year
    # Fri, 24 Dec 2010 00:00:00 +0000

### beginning_of_day
#### 説明
今日の初めの時刻を取得

#### 使い方
    <日時>.beginning_of_day

#### 例
##### 今日の初めの時刻を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).beginning_of_day
    # Sat, 24 Dec 2011 00:00:00 +0000

### end_of_day
#### 説明
今日の終わりの時刻を取得

#### 使い方
    <日時>.end_of_day

#### 例
##### 今日の1秒後の時刻を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).end_of_day
    # Sat, 24 Dec 2011 23:59:59 +0000

### ago
#### 説明
今日の○秒前の時刻を取得

#### 使い方
    <日時>.ago(秒数)

#### 例
##### 今日の1秒前の時刻を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).ago(1)
    # Sat, 23 Dec 2011 23:59:59 +0000

### since
#### 説明
今日の○秒後の時刻を取得

#### 使い方
    <日時>.since(秒数)

#### 例
##### 今日の1秒後の時刻を取得
    DateTime.new(2011, 12, 24, 00, 00, 00).since(1)
    # Sat, 24 Dec 2011 00:00:01 +0000

### seconds_since_midnight
#### 説明
今日の0時からの秒数を取得

#### 使い方
    <日時>.seconds_since_midnight

#### 例
##### 今日の0時からの秒数を取得
    DateTime.new(2011, 12, 24, 10, 00, 00).seconds_since_midnight
    # 36000

### utc
#### 説明
UTCの日時を取得

#### 使い方
    <日時>.seconds_since_midnight

#### 例
##### UTCの日時を取得
    DateTime.current.utc # Sat, 24 Dec 2011 00:00:00 +0900
    # Fir, 23 Dec 2011 09:00:00 +1500