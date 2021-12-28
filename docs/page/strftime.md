---
layout: page
---

### 説明

時刻をフォーマットに従って文字列に変換

### 使い方

    strftime(フォーマット)

### フォーマット

| フォーマット | 説明                                                                                                       |
| ------------ | ---------------------------------------------------------------------------------------------------------- |
| %A           | 曜日の名称(Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday)                                 |
| %a           | 曜日の省略名(Sun, Mon, Tue, Wed, Thu, Fri, Sat)                                                            |
| %B           | 月の名称(January, February, March, April, May, June, July, August, September, October, November, December) |
| %b           | 月の省略名(Jan, Feb, Mar, Aprm May, Jun, Jul, Aug, Sep, Oct, Nov, Dec)                                     |
| %c           | 日付と時刻                                                                                                 |
| %d           | 日(01-31)                                                                                                  |
| %H           | 24時間制の時(00-23)                                                                                        |
| %I           | 12時間制の時(01-12)                                                                                        |
| %j           | 年中の通算日(001-366)                                                                                      |
| %M           | 分(00-59)                                                                                                  |
| %m           | 月を表す数字(01-12)                                                                                        |
| %p           | 午前または午後(AM,PM)                                                                                      |
| %S           | 秒(00-60) (60はうるう秒)                                                                                   |
| %U           | 週を表す数。最初の日曜日が第1週の始まり(00-53)                                                             |
| %W           | 週を表す数。最初の月曜日が第1週の始まり(00-53)                                                             |
| %w           | 曜日を表す数。日曜日が0(0-6)                                                                               |
| %X           | 時刻                                                                                                       |
| %x           | 日付                                                                                                       |
| %Y           | 西暦を表す数                                                                                               |
| %y           | 西暦の下2桁(00-99)                                                                                         |
| %Z           | タイムゾーン                                                                                               |
| %%           | パーセント文字                                                                                             |

### 例

#### 日本語で秒数まで表示

    time = Time.now # Thu Dec 24 00:00:00 +0900 2011
    time.strftime('%Y年%m月%d日 %H:%M:%S')
    # 2011年12月24日 00:00:00

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activesupport/lib/active_support/time_with_zone.rb#L255)
