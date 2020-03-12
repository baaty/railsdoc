---
layout: archive_page
---
### 説明
読み込み専用としてモデルを取得

### 使い方
    モデル.readonly(値)

### 例
#### 読み込み専用としてモデルを取得
    users = User.readonly
    users.first.save
    # ActiveRecord::ReadOnlyRecord: ActiveRecord::ReadOnlyRecord

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/query_methods.rb#L746)