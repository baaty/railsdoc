---
layout: page
---

### 説明

よく利用する検索条件をあらかじめ準備

### 使い方

    scope(スコープ名, 条件式、ブロック引数)

### 例

    scope :rails_base, where(category: "rails_base")
    Page.rails_base

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/routing/mapper.rb#L825)
