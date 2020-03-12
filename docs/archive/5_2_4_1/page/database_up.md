---
layout: archive_page
---
### 説明
データベースのカラムをバージョンアップ  
upメソッドはロールバックできない処理をする際に主に使用

### 使い方
    def up
    end

### 例
#### pagesテーブルにnameカラムをstring型で作成
    def up
      create_table :pages do |t|
        t.string :name
        t.string :category
      end
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/migration.rb#L774)