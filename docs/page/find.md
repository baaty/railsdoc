---
layout: page
---
### 説明
データベースから指定したIDのレコードを取得

### 使い方
    モデル.find(件数)

### 例
    Person.find(1)
    # returns the object for ID = 1

    Person.find("1")
    # returns the object for ID = 1

    Person.find("31-sarah")
    # returns the object for ID = 31

    Person.find(1, 2, 6)
    # returns an array for objects with IDs in (1, 2, 6)

    Person.find([7, 17])
    # returns an array for objects with IDs in (7, 17)

    Person.find([1])
    # returns an array for the object with ID = 1

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/finder_methods.rb#L67)