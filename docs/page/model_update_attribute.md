---
layout: page
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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/persistence.rb#L605)