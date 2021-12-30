---
layout: page
---

### 説明

指定したテーブルに外部キー制約を追加

### 使い方

    add_foreign_key(参照元テーブル名, 参照先テーブル名, オプション引数)

### オプション

| オプション     | 説明                                             | 初期値                        |
| -------------- | ------------------------------------------------ | ----------------------------- |
| :column        | 外部キーカラム名                                 | to_table.singularize + "\_id" |
| :primary_key   | 参照先テーブルの主キー                           | id                            |
| :name          | 制約                                             | fk_rails_\<identifier\>         |
| :on_delete     | 削除時のアクション                               |                               |
| :on_update     | 更新時のアクション                               |                               |
| :if_not_exists | 外部キーがすでに存在する場合は再追加しない       |                               |
| :validate      | バリデート(PostgreSQLのみ)                       | true                          |
| :deferrable    | 外部キーが遅延可能かどうかを指定(PostgreSQLのみ) | false                         |

### 例

#### 外部キー制約を追加

    add_foreign_key :articles, :authors
    # ALTER TABLE "articles" ADD CONSTRAINT fk_rails_e74ce85cbc FOREIGN KEY ("author_id") REFERENCES "authors" ("id")

#### 主キーを指定

    add_foreign_key :articles, :users, column: :author_id, primary_key: "lng_id"
    # ALTER TABLE "articles" ADD CONSTRAINT fk_rails_58ca3d3a82 FOREIGN KEY ("author_id") REFERENCES "users" ("lng_id")

#### 削除時のアクションを指定

    add_foreign_key :articles, :authors, on_delete: :cascade
    # ALTER TABLE "articles" ADD CONSTRAINT fk_rails_e74ce85cbc FOREIGN KEY ("author_id") REFERENCES "authors" ("id") ON DELETE CASCADE

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L1085)
