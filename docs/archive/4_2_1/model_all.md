---
layout: page
---
### 説明
テーブルからすべてのレコードを取得する

### 使い方
    モデル.all

### 例
#### Pagesテーブルからすべてのレコードを取得
    Page.all
    # SELECT "pages".* FROM "pages"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/b1879124a82b34168412ac699cf6f654e005c4d6/activerecord/lib/active_record/scoping/named.rb#L24)