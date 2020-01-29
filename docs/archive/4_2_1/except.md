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
* [GitHub](https://github.com/rails/rails/blob/f5a635e4f47f5c864d49e8fe23641d65adfb25e3/activerecord/lib/active_record/relation/spawn_methods.rb#L52)