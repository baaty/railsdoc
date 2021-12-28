---
layout: page
---
### 説明
指定した条件に一致するレコードをSQLを直接実行して全て削除  
関連付けられたモデルは削除しない

### 使い方
    モデル.delete_all([検索条件])

### 例
#### 全てのレコードを削除
    person.pets.delete_all

#### 条件を指定
    person.pets.delete_all("id > 0")

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/associations/collection_proxy.rb#L471)