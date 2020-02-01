---
layout: page
---
### 説明
外部キー制約を追加

### 使い方
    add_foreign_key(テーブル名, 参照先テーブル名 [, オプション])

### オプション

オプション | 説明
------- | -------
:column | 外部キーカラム名
:primary_key | 参照先テーブルの主キー
:name | 制約
:on_delete | 削除時のアクション
:on_update | 更新時のアクション
:validate | バリデート

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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L991)