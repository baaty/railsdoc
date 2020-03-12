---
layout: archive_page
---
### 説明
引数で指定した件数のレコードを取得  
取得するレコードをIDなどで指定することはできない

### 使い方
    モデル.take([件数])

#### 取得するレコードが存在しない場合に例外が発生
    モデル.take!([件数])

### 例
#### 1件のレコードを取得
    Person.take
    # <Person id: 1, ...>
    # SQL: SELECT * FROM people LIMIT 1

#### 2件のレコードを取得
    Person.take(2)
    # [
    #   <Client id: 1, ...>,
    #   <Client id: 220, ...>
    # ]
    # SQL: SELECT * FROM people LIMIT 5

#### whereの後に使用
    Person.where(["name LIKE '%?'", name]).take

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/associations/collection_proxy.rb#L289)