---
layout: page
---
### 配列とは
インデックスを使って、複数のオブジェクトへの参照をまとめて管理することができるオブジェクト

### メソッド
#### sampleメソッド
##### 使い方
    配列.sample(個数)

##### 説明
配列から、ランダムにn個の要素を取り出す。Ruby1.9以降

##### 例
    [1, 2, 3, 4, 5, 6, 7].sample(2)
    # [3, 1]

#### keep_ifメソッド
##### 使い方
    配列.keep_if {|arr| 条件式 }

##### 説明
配列から、条件を満たさない要素を削除。Ruby1.9以降

##### 例
    ["ipad", "iPhone", "ipod", "iTunes", "Android"].keep_if {|i| i =~ /^i/ }
    # ["ipad", "iPhone", "ipod", "iTunes"]

#### repeated_combinationメソッド
##### 使い方
    配列.repeated_combination(個数) {|arr| block }

##### 説明
配列から、任意の○個の重複の組み合わせを列挙する。Ruby1.9以降

#### repeated_permutationメソッド
##### 使い方
    配列.repeated_permutation(個数) {|arr| block }

##### 説明
配列から、任意の○個からなる重複順列を列挙する。Ruby1.9以降

#### rotateメソッド
##### 使い方
    配列.rotate(個数)

##### 説明
配列から、要素を回転させるようにして要素をずらした配列。Ruby1.9以降