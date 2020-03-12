---
layout: archive_page
---
### 説明
モデルの変更前と変更後の値をハッシュで取得

### 使い方
    モデル.changes()

### 例
    person.changes # {}
    person.name = 'bob'
    person.changes # {name: ["bill", "bob"]}

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activemodel/lib/active_model/dirty.rb#L234)