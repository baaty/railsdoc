---
layout: page
---

### 説明

マイグレーションのロールバック

### 使い方

    revert(マイグレーションクラス.., ブロック引数)

### 例

    class FixTLMigration < ActiveRecord::Migration[7.0]
        def change
            revert do
                create_table(:horses) do |t|
                    t.text :content
                    t.datetime :remind_at
                end
            end
            create_table(:apples) do |t|
                t.string :variety
            end
        end
    end

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/migration.rb#L731)
