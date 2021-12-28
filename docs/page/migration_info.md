---
layout: page
---

### 説明

直接SQLを使わずにデータベースのテーブルやカラムなどの構造を変更できる仕組み

### 簡単な例

    class CreateProducts < ActiveRecord::Migration[7.0]
      def change
        create_table :products do |t|
          t.string :name
          t.text :description

          t.timestamps
        end
      end
    end

### 昔からある記述方法

changeの代わりにupとdownで書くことも可能

    class CreateProducts < ActiveRecord::Migration[7.0]
      def up
        create_table :products do |t|
          t.string :name
          t.text :description

          t.timestamps
        end
      end

      def down
        drop_table :products
      end
    end