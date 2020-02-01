---
layout: page
---
### 説明
分割してレコードを取得して処理
デフォルトで1000件ずつ処理

### 使い方
    モデル.find_in_batches([オプション]) do |i|
    end

### オプション

オプション            | 説明         | デフォルト値
-----------------|------------|-------
:batch_size      | 同時処理数   | 1000
:start           | 処理開始位置 |
:finish          | 終了するときのキー  |
:error_on_ignore | 例外を発生させる |

### 例
#### 分割してレコードを取得して処理
    Person.where("age > 21").find_in_batches do |group|
      sleep(50) # Make sure it doesn't get too crowded in there!
      group.each { |person| person.party_all_night! }
    end

#### 同時処理数を2000
    Person.all.find_in_batches(start: 2000, batch_size: 2000) do |group|
      group.each { |person| person.party_all_night! }
    end

### 補足
* 処理する順序は指定できない
* find_eachとの違いは配列で値を受けとること
* 順番に処理したい場合は、find_eachを使用

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/batches.rb#L126)