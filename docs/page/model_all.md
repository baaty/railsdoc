---
layout: page
---
### 説明
テーブルからすべてのレコードを取得

### 使い方
    モデル.all

### 例
#### Pagesテーブルからすべてのレコードを取得
    Page.all
    # SELECT "pages".* FROM "pages"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/scoping/named.rb#L26)