---
layout: page
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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/query_methods.rb#L814)