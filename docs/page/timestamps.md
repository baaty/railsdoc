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
      t.timestamps
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L593)