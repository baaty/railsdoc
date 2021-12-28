---
layout: page
---

### 説明

与えられたクラスメソッドが与えられたコンテンツに存在することを確認

### 使い方

    assert_class_method(メソッド, コンテンツ, ブロック引数)

### 例

    assert_migration "db/migrate/create_products.rb" do |migration|
        assert_class_method :up, migration do |up|
            assert_match(/create_table/, up)
        end
    end

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/railties/lib/rails/generators/testing/assertions.rb#L88)
