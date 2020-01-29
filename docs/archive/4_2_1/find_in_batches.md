---
layout: page
---
### 説明
分割してレコードを取得して処理をする
デフォルトで1000件ずつ処理をする

### 使い方
    モデル.find_in_batches([オプション]) do |i|
    end

### オプション

オプション       | 説明
----------- | ------
:start      | 処理開始位置
:batch_size | 同時処理数

### 例
    Person.where("age > 21").find_in_batches do |group|
      sleep(50) # Make sure it doesn't get too crowded in there!
      group.each { |person| person.party_all_night! }
    end

    Person.all.find_in_batches(start: 2000, batch_size: 2000) do |group|
      group.each { |person| person.party_all_night! }
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/2a7cf24cb7aab28f483a6772b608e2868a9030ba/activerecord/lib/active_record/relation/batches.rb#L98)