---
layout: page
---

### 説明

IDを指定してレコードを取得  
指定したIDの中に存在しないIDが1つでもあると例外が発生

### 使い方

    モデル.find(件数..)

### 例

#### IDを指定してレコードを取得

    Person.find(1)

#### 複数IDを指定

    Person.find(1, 2, 6)

#### 配列で指定

    Person.find([7, 17])

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/finder_methods.rb#L67)
