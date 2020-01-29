---
layout: page
---
### 説明
created_atとupdated_atを両方追加するメソッド

### 使い方
    timestamps

### 例
#### usersテーブルにtimestampsを設定
    create_table :users do |t|
    &nbsp;&nbsp;t.timestamps
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0230ad686118b60e89ef8cd2f7b2936099de6deb/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L481)