---
layout: page
---
### 説明
データベースのカラムをバージョンアップ
Rails3.0以下のバージョンのself.upに相当するのは、changeメソッド
Rails3.1以上で、upメソッドはロールバックできない処理をする際に主に使用

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