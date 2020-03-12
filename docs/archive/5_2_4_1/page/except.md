---
layout: archive_page
---
### 説明
モデルに適応した条件式を除外

### 使い方
    モデル.except(条件式)

### 例
#### orderによる並び替えを除外
    Page.order("category DESC").except(:order)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/spawn_methods.rb#L57)