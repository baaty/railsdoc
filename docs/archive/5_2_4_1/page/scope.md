---
layout: archive_page
---
### 説明
よく利用する検索条件をあらかじめ準備

### 使い方
    scope(スコープ名, 条件式)

### 例
#### rails_baseカテゴリのデータだけを取得するスコープ
    scope :rails_base, where(category: "rails_base")
    Page.rails_base

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionpack/lib/action_dispatch/routing/mapper.rb#L833)