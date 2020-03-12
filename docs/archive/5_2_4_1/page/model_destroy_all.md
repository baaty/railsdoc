---
layout: archive_page
---
### 説明
ActiveRecordを使って指定した条件の全てのレコードを削除  
dependentが設定されている場合は関連付けられたモデルも削除

### 使い方
    モデル.destroy_all([検索条件])

### 例
#### 条件を指定して削除
    Person.destroy_all("last_login < '2004-04-04'")

#### 条件を指定して削除
    Person.destroy_all(status: "inactive")

#### 全て削除
    Person.where(age: 0..18).destroy_all

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/associations/collection_proxy.rb#L501)