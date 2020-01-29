---
layout: page
---
### 説明
指定したテーブルのカラム名を変更
名前を変更しても、そのカラムに関連付けられている既存のデータは破棄されない

### 使い方
    rename_column(テーブル名, 変更するカラム名, 新しいカラム名)

    change_table テーブル名 do |t|
    &nbsp;&nbsp;t.rename 変更するカラム名, 新しいカラム名
    end

### 例
#### usersテーブルのe_mailカラムをmailに変更
    class RenameEmailColumn < ActiveRecord::Migration
      def self.up
        rename_column :users, :e_mail, :mail
      end
      def self.down
        rename_column :users, :mail, :e_mail
      end
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/9985da0856bad47d25a0bf6cc34474cd69f1b77c/activerecord/lib/active_record/connection_adapters/postgresql/schema_statements.rb#L471)