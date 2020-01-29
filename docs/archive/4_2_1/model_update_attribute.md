---
layout: page
---
### 説明
属性ハッシュを指定して更新

### 使い方
    モデル.update_attribute = { カラム名 = 値 }

### 例

#### 属性の変更・保存メソッド
    @user.update_attribute = { :username = 'A' }

### 更新メソッドの種類

メソッド              | バリデーションによる検証の有無
----------------- | ---------------
update            | ○
update_all        | ×
update_attributes | ○
update_attribute  | ×