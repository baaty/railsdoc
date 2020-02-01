---
layout: page
---
### 説明
カラムのコメントを変更または削除

### 使い方
    change_column_comment(table_name, column_name, comment_or_changes)

### 例
#### カラムのコメントを変更
    change_column_comment :posts, :state, from: "old_comment", to: "new_comment"

#### カラムのコメントを削除
    change_column_comment :posts, :state, nil

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L1224)