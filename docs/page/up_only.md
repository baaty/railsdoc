---
layout: page
---

### 説明

マイグレーションアップ時にのみ実行される処理

### 使い方

    up_only(ブロック引数)

### 例

    class AddPublishedToPosts < ActiveRecord::Migration[7.0]
        def change
            add_column :posts, :published, :boolean, default: false
            up_only do
                execute "update posts set published = 'true'"
            end
        end
    end

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/migration.rb#L807)
