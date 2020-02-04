---
layout: page
---
### 説明
引数で指定した件数のレコードを取得

### 使い方
    モデル.take([件数])

### 例
#### 1件のレコードを取得
    Person.take
    # returns an object fetched by SELECT * FROM people LIMIT 1

#### 5件のレコードを取得
    Person.take(5)
    # returns 5 objects fetched by SELECT * FROM people LIMIT 5

#### whereの後に使用
    Person.where(["name LIKE '%?'", name]).take

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/associations/collection_proxy.rb#L286)