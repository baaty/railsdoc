---
layout: page
---
### 説明
配列関係の便利関数

### deep_dup
#### 説明
配列のディープコピー

#### 使い方
    配列.deep_dup

#### 例
    array = [1, [2, 3]]
    dup   = array.deep_dup
    dup[1][2] = 4
    array[1][2] # nil
    dup[1][2]   # 4

### excluding
#### 説明
指定された要素を除外した配列

#### 使い方
    配列.excluding(要素)

#### 例
##### 文字列の配列から特定の文字列を除外
    ["David", "Rafael", "Aaron", "Todd"].excluding("Aaron", "Todd")
    # ["David", "Rafael"]

##### 配列の配列から特定の配列を除外
    [ [ 0, 1 ], [ 1, 0 ] ].excluding([ [ 1, 0 ] ])
    # [ [ 0, 1 ] ]

### excluding!
#### 説明
指定された要素を除外した配列
excludingの破壊的メソッド版

#### 使い方
    配列.excluding!(要素)

#### 例
##### 文字列の配列から特定の文字列を除外
    ["David", "Rafael", "Aaron", "Todd"].excluding!("Aaron", "Todd")
    # ["David", "Rafael"]

##### 配列の配列から特定の配列を除外
    [ [ 0, 1 ], [ 1, 0 ] ].excluding!([ [ 1, 0 ] ])
    # [ [ 0, 1 ] ]

### from
#### 説明
配列の末尾から指定された位置までの配列

#### 使い方
    配列.from(位置)

#### 例
##### 全配列
    %w( a b c d ).from(0)
    # ["a", "b", "c", "d"]

##### 最後の2個の配列
    %w( a b c d ).from(2)
    # ["c", "d"]

##### 配列数より大きな数を指定
    %w( a b c d ).from(10)
    # []

##### 空の配列
    %w().from(0)
    # []

### in_groups
#### 説明
指定した数の配列にグルーピング

#### 使い方
    配列.in_groups(数, 埋める文字列)

#### 例
##### グルーピング
    %w(1 2 3 4 5 6 7 8 9 10).in_groups(3) {|group| p group}
    # ["1", "2", "3", "4"]
    # ["5", "6", "7", nil]
    # ["8", "9", "10", nil]

##### 埋める文字列を指定
    %w(1 2 3 4 5 6 7 8 9 10).in_groups(3, '&nbsp;') {|group| p group}
    # ["1", "2", "3", "4"]
    # ["5", "6", "7", "&nbsp;"]
    # ["8", "9", "10", "&nbsp;"]

### in_groups_of
#### 説明
指定した長さの配列にグルーピング

#### 使い方
    配列.in_groups_of(数, 埋める文字列)

#### 例
##### グルーピング
    %w(1 2 3 4 5 6 7 8 9 10).in_groups_of(3) {|group| p group}
    # ["1", "2", "3"]
    # ["4", "5", "6"]
    # ["7", "8", "9"]
    # ["10", nil, nil]

##### 埋める文字列を指定
    %w(1 2 3 4 5).in_groups_of(2, '&nbsp;') {|group| p group}
    # ["1", "2"]
    # ["3", "4"]
    # ["5", "&nbsp;"]

### including
#### 説明
配列に要素を追加

#### 使い方
    配列.including(要素)

#### 例
##### 配列に要素を追加
    [ 1, 2, 3 ].including(4, 5)
    # [ 1, 2, 3, 4, 5 ]

##### 配列の配列を追加
    [ [ 0, 1 ] ].including([ [ 1, 0 ] ])
    # [ [ 0, 1 ], [ 1, 0 ] ]

### inquiry
#### 説明
配列をオブジェクトに変換

#### 使い方
    配列.inquiry

#### 例
    pets = [:cat, :dog].inquiry
    pets.cat?     # true
    pets.ferret?  # false

### split
#### 説明
配列を分割

#### 使い方
    配列.split(値)

#### 例
##### 配列を分割
    [1, 2, 3, 4, 5].split(3)
    # [[1, 2], [4, 5]]

##### 配列の条件を指定して分割
    (1..10).to_a.split { |i| i % 3 == 0 }
    # [[1, 2], [4, 5], [7, 8], [10]]

### to
#### 説明
初めから位置までの配列

#### 使い方
    配列.to(位置)

#### 例
##### 配列の先頭を取得
    %w( a b c d ).to(0)
    # ["a"]

##### 配列の先頭から3個取得
    %w( a b c d ).to(2)
    # ["a", "b", "c"]

##### 配列より大きな数を指定
    %w( a b c d ).to(10)
    # ["a", "b", "c", "d"]

##### 空の配列
    %w().to(0)
    # []

### to_query
#### 説明
キーからURLで使える文字列

#### 使い方
    配列.to_query(キー名)

#### 例
    ['Rails', 'coding'].to_query('hobbies')
    # "hobbies%5B%5D=Rails&hobbies%5B%5D=coding"

### to_sentence
#### 説明
英文として適した文字列

#### 使い方
    配列.to_sentence([オプション])

#### オプション

オプション                | 説明                          | デフォルト値
---------------------|-------------------------------|--------
:words_connector     | 3つ以上の場合の最後以外の結合文字 | ,
:two_words_connector | 結合文字                      | " and”
:last_word_connector | 3つ以上の場合は最後の結合文字     | “, and”
:locale              | ロケール                          |

#### 例
##### 空の配列
    [].to_sentence
    # ""

##### 配列の要素が1
    ['one'].to_sentence
    # "one"

##### 配列の要素が2
    ['one', 'two'].to_sentence
    # "one and two"

##### 配列の要素が3
    ['one', 'two', 'three'].to_sentence
    # "one, two, and three"

### to_xml
#### 説明
XML変換

#### 使い方
    配列.to_xml([オプション])

#### 例
    [{ foo: 1, bar: 2}, { baz: 3}].to_xml
    # <?xml version="1.0" encoding="UTF-8"?>
    # <objects type="array">
    #   <object>
    #     <bar type="integer">2</bar>
    #     <foo type="integer">1</foo>
    #   </object>
    #   <object>
    #     <baz type="integer">3</baz>
    #   </object>
    # </objects>

### sum
#### 説明
合計値を計算

#### 使い方
    配列.sum

#### 例
##### 1から10までの合計値
    [1,2,3,4,5,6,7,8,9,10].sum

### sum(Ruby)
#### 説明
条件を満たす値の合計値を計算

#### 使い方
    配列.sum{|n| 条件}

#### 例
##### 1から10まで偶数の合計値
    [1,2,3,4,5,6,7,8,9,10].sum{|num| num %2 == 0}