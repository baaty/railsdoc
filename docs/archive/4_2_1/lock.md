---
layout: page
---
### 楽観的ロック
あらかじめカラムのロックバージョンを記録しておき、更新時にロックバージョンが変わっていないことを検証して保存

    class CreateAddLockColumnToEntries < ActiveRecord::Migration
      def self.up
        create_table :add_lock_column_to_entries do |t|
          t.integer :entries, :lock_version, :null => false, :default => 0
        end
      end

      def self.down
        drop_table :add_lock_column_to_entries
      end
    end

### 悲観的ロック
データベース側でレコードをロックし、並行に更新できないようにする

    locked_entry = Entry.find(１，:lock => true)

* MySQLとPostgreSQLでのみ利用可能