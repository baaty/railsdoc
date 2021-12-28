---
layout: page
---
### 説明
モデルに適応した条件式を除外

### 使い方
    モデル.except(条件式)

### 例
#### orderによる並び替えを除外
    Page.order("category DESC").except(:order)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/spawn_methods.rb#L57)