---
layout: page
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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_dispatch/routing/mapper.rb#L841)