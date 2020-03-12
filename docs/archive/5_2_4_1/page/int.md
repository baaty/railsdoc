---
layout: archive_page
---
### 説明
数値関係の便利関数

### months
#### 説明
月の形式に変換

#### 使い方
    数字.months

#### 例
    2.months
    # 2 months

### multiple_of?
#### 説明
割り切れるか？

#### 使い方
    数字.multiple_of?(数字)

#### 例
    0.multiple_of?(0)
    # true

    6.multiple_of?(5)
    # false

    10.multiple_of?(2)
    # true

### ordinal
#### 説明
順番のサフィックス

#### 使い方
    数字.ordinal

#### 例
    1.ordinal
    # "st"

    2.ordinal
    # "nd"

    1002.ordinal
    # "nd"

    1003.ordinal
    # "rd"

    -11.ordinal
    # "th"

    -1001.ordinal
    # "st"

### ordinalize
#### 説明
数字を順序文字列に変換

#### 使い方
    数字.ordinalize

#### 例
    1.ordinalize
    # "1st"

    2.ordinalize
    # "2nd"

    1002.ordinalize
    # "1002nd"

    1003.ordinalize
    # "1003rd"

    -11.ordinalize
    # "-11th"

    -1001.ordinalize
    # "-1001st"

### years
#### 説明
年の形式に変換

#### 使い方
    数字.years

#### 例
    2.years
    # 2 years