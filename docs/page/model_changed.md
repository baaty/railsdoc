---
layout: page
---
### 説明
属性の変更点を取得

### 使い方
    モデル.changed

### 例
    person.changed # []
    person.name = 'bob'
    person.changed # ["name"]

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activemodel/lib/active_model/dirty.rb#L164)