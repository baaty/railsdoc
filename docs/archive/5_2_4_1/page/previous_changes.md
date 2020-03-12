---
layout: archive_page
---
### 説明
保存される前に変更された値をハッシュで取得

### 使い方
    モデル.previous_changes()

### 例
#### 保存される前に変更された値をハッシュで取得
    person.name # "bob"
    person.name = 'robert'
    person.save
    person.previous_changes # {name: ["bob", "robert"]}

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activemodel/lib/active_model/dirty.rb#L227)