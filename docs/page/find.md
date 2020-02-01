---
layout: page
---
### 説明
指定したIDのレコードを取得

### 使い方
    モデル.find(件数)

### 例
#### 指定したIDのレコードを取得
    Person.find(1)
    # returns the object for ID = 1

#### 複数IDを指定
    Person.find(1, 2, 6)
    # returns an array for objects with IDs in (1, 2, 6)

#### 配列で指定
    Person.find([7, 17])
    # returns an array for objects with IDs in (7, 17)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/finder_methods.rb#L67)