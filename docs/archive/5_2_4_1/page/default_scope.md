---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/scoping/default.rb#L89)