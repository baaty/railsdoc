---
layout: archive_page
---
### 説明
created_atとupdated_atを両方追加するメソッド

### 使い方
    timestamps

### 例
#### usersテーブルにtimestampsを設定
    create_table :users do |t|
      t.timestamps
    end

### ソースコード
* [GitHub](https://api.rubyonrails.org/v5.2.4.1/classes/ActiveRecord/ConnectionAdapters/SchemaStatements.html#method-i-add_timestamps)