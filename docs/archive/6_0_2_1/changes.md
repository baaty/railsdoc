---
layout: page
---
### 説明
モデルの変更前と変更後の値をハッシュで取得

### 使い方
    モデル.changes

### 例
    person.changes # {}
    person.name = 'bob'
    person.changes # {name: ["bill", "bob"]}

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activemodel/lib/active_model/dirty.rb#L217)