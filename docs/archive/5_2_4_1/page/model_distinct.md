---
layout: archive_page
---
### 説明
重複のない値を取得

### 使い方
    モデル.distinct([重複を削除するか])

### 例
#### 重複のない値を取得
    User.select(:name).distinct

#### 重複も削除
    User.select(:name).distinct(false)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/associations/collection_proxy.rb#L723)