---
layout: page
---

### 説明

データベースのカラムをバージョンアップ  
upメソッドはロールバックできない処理をする際に主に使用

### 使い方

    def up
    end

### 例

    def up
      create_table :pages do |t|
        t.string :name
        t.string :category
      end
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/migration.rb#L829)
