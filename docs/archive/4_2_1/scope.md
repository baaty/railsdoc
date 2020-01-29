---
layout: page
---
### 説明
よく利用する検索条件をあらかじめ準備

### 使い方
    scope(スコープ名, 条件式)

### 例
#### rails_baseカテゴリのデータだけを取得するスコープ
    scope :rails_base, where(:category => "rails_base")
    Page.rails_base

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f5d2f3fc759ec9a942609ca5b8446e83fdf869b4/actionpack/lib/action_dispatch/routing/mapper.rb#L779)