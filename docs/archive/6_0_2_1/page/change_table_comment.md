---
layout: page
---
### 説明
テーブルのコメントの変更または削除

### 使い方
    change_table_comment(テーブル名, コメント)

### 例
#### テーブルのコメントの変更
    change_table_comment :posts, from: "old_comment", to: "new_comment"

#### テーブルのコメントの削除
    change_table_comment :posts, nil

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L1214)