---
layout: page
---
### 説明
読み込み専用として、モデルオブジェクトを取得

### 使い方
    モデル.readonly(値)

### 例
    users = User.readonly
    users.first.save
    => ActiveRecord::ReadOnlyRecord: ActiveRecord::ReadOnlyRecord

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0399b71dab8b270b4e40b2aff99194a8b8f2596c/activerecord/lib/active_record/relation/query_methods.rb#L704)