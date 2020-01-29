---
layout: page
---
### 説明
データベースから取得したオブジェクトを更新

### 使い方
    モデル.update(カラム名 = 値)

### 例
#### データを更新
    User.update("name = 'A'")

### 更新メソッドの種類

メソッド              | バリデーションによる検証の有無
----------------- | ---------------
update            | ○
update_all        | ×
update_attributes | ○
update_attribute  | ×

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/78bd18a90992e3da767cfe492f1bc5d63077da8a/activerecord/lib/active_record/relation.rb#L363)