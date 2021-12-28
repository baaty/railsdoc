---
layout: page
---

### 説明

ロールバックする方法がわからない処理

### 使い方

    reversible()

### 例

    class SplitNameMigration < ActiveRecord::Migration[7.0]
        def change
            add_column :users, :first_name, :string
            add_column :users, :last_name, :string

            reversible do |dir|
                User.reset_column_information
                User.all.each do |u|
                    dir.up   { u.first_name, u.last_name = u.full_name.split(' ') }
                    dir.down { u.full_name = "#{u.first_name} #{u.last_name}" }
                    u.save
                end
            end

            revert { add_column :users, :full_name, :string }
        end
    end

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/migration.rb#L788)
