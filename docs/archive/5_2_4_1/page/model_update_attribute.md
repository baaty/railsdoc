---
layout: archive_page
---
### 説明
条件に一致するモデルオブジェクトを更新  
バリデーションはスキップ

### 使い方
    モデル.update_attribute(属性名, 値)

### 例
#### 条件に一致するレコードを更新
    @user.update_attribute(:name, "hoge")

### 更新メソッドの種類

メソッド              | バリデーションによるバリデーションの有無
----------------- | ---------------
update            | ○
update_all        | ×
update_attributes | ○
update_attribute  | ×

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/persistence.rb#L412)