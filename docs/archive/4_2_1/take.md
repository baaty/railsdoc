---
layout: page
---
### 説明
引数で指定した件数のレコードを取得

### 使い方
    モデル.take([件数])

### 例
    Person.take
    # returns an object fetched by SELECT * FROM people LIMIT 1

    Person.take(5)
    # returns 5 objects fetched by SELECT * FROM people LIMIT 5

    Person.where(["name LIKE '%?'", name]).take

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/430a09514a4ad1d0f8481f18a42c4813b6b61e38/activerecord/lib/active_record/relation/finder_methods.rb#L104)