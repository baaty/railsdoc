---
layout: page
---
### 説明
デフォルトのスコープを定義

### 使い方
    default_scope(条件式 [, ブロック])

### 例
#### whereを付与
    class Article < ActiveRecord::Base
      default_scope { where(published: true) }
    end
    Article.all
    # SELECT * FROM articles WHERE published = true

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/scoping/default.rb#L89)