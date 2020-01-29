---
layout: page
---
### 説明
直接SQLを使わずに、データベースのテーブルやカラムなどの構造を変更できる仕組み

### 特徴
* db/migrateディレクトリ以下にあるRubyで書かれたファイル
* ファイル名はタイムスタンプ(西暦、月、日、時、分、秒)とアンダースコア(_)で始まり、クラス名のすべての大文字を小文字にしたもの
* 別々のマイグレーションファイルに同じ名前のマイグレーションクラスを記述できない
* idという主キーを自動的に追加
* 実行するにはRakeタスク
* schema_infoテーブルに現在のバージョンが格納

### 簡単な例
    class AddSsl < ActiveRecord::Migration
      def up
        add_column :accounts, :ssl_enabled, :boolean, default: true
      end

      def down
        remove_column :accounts, :ssl_enabled
      end
    end

    class TenderloveMigration < ActiveRecord::Migration
      def change
        create_table(:horses) do |t|
          t.column :content, :text
          t.column :remind_at, :datetime
        end
      end
    end

### 利用可能なメソッド
* create_table
* drop_table
* change_table
* rename_table
* add_column
* rename_column
* change_column
* remove_column
* add_index
* remove_index
* remove_index

### サポートしているデータベース
* MySQL
* PostgreSQL
* SQLite
* SQL Server
* Sybase
* Oracle