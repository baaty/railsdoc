---
layout: archive_page
---
### 説明
カラムのコメントを変更または削除

### 使い方
    change_column_comment(テーブル名, カラム名, comment_or_changes)

### 例
#### カラムのコメントを変更
    change_column_comment :posts, :state, from: "old_comment", to: "new_comment"

#### カラムのコメントを削除
    change_column_comment :posts, :state, nil

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L1177)