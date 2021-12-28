---
layout: page
---

### 説明

データベースのカラムをバージョンダウン  
ロールバックできない処理の際に主に使用

### 使い方

    def down
    end

### 例

    def down
      drop_table :pages
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/migration.rb#L835)
