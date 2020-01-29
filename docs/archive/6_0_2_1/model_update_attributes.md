---
layout: page
---
### 説明
属性ハッシュを指定して更新

### 使い方
    モデル.update_attributes = { カラム名 = 値 }

### 例
#### 複数の項目を一度に変更・保存するメソッド
    @user.update_attributes = { :username = 'A', :category = 'B' }

### 更新メソッドの種類

メソッド              | バリデーションによる検証の有無
----------------- | ---------------
update            | ○
update_all        | ×
update_attributes | ○
update_attribute  | ×

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/persistence.rb#L616)