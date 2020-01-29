---
layout: page
---
### 説明
分割してレコードを取得して処理をする
デフォルトで1000件ずつ処理をする

### 使い方
    モデル.find_each([オプション]) do |i|
    end

### オプション

オプション       | 説明
----------- | ------
:start      | 処理開始位置
:batch_size | 同時処理数

### 例
#### category_idが1の値をeachする
    Page.where(:category_id => 1).find_each do |page|

    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/2a7cf24cb7aab28f483a6772b608e2868a9030ba/activerecord/lib/active_record/relation/batches.rb#L48)