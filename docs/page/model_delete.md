---
layout: page
---
### 説明
指定した条件に一致するレコードをSQLを直接実行して削除  
関連付けられたモデルは削除しない

### 使い方
    モデル.delete(条件)

### 例
#### レコードを削除
    person.pets.delete(Pet.find(1))
    # [<Pet id: 1, name: "Fancy-Fancy", person_id: 1>]

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/associations/collection_proxy.rb#L617)