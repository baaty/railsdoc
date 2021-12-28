---
layout: page
---
### 説明
whereやorderなどで取得済みのモデルから先頭のレコードの値を1件取得  
relation.limit(1).pluck(*column_names).firstの省略形

### 使い方
    pick(カラム名 [, ...])

### 例
#### 先頭のレコードの値を1件取得
    User.where(id: 1).pick(:name)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/calculations.rb#L212)