---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/associations/collection_proxy.rb#L620)