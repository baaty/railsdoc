---
layout: page
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

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L1398)
