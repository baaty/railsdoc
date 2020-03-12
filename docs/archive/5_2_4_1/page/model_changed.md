---
layout: archive_page
---
### 説明
変更点を取得

### 使い方
    モデル.changed()

### 例
    person.changed # []
    person.name = 'bob'
    person.changed # ["name"]

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activemodel/lib/active_model/dirty.rb#L170)