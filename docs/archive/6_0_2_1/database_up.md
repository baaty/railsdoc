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
#### pagesテーブルにnameカラムをstring型で作成
    def up
      create_table :pages do |t|
        t.string :name
        t.string :category
      end
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/migration.rb#L788)