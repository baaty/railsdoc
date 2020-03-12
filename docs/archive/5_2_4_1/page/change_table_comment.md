---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L1172)