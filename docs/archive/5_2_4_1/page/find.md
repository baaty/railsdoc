---
layout: archive_page
---
### 説明
IDを指定してレコードを取得  
指定したIDの中に存在しないIDが1つでもあると例外が発生

### 使い方
    モデル.find(件数)

### 例
#### IDを指定してレコードを取得
    Person.find(1)
    # <Person id: 1, ...>

#### 複数IDを指定
    Person.find(1, 2, 6)
    # [
    #   <Person id: 1, ...>,
    #   <Person id: 2, ...>,
    #   <Person id: 6, ...>
    # ]

#### 配列で指定
    Person.find([7, 17])
    # [
    #   <Person id: 7, ...>,
    #   <Person id: 17, ...>
    # ]

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/finder_methods.rb#L67)