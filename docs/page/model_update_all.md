---
layout: page
---
### 説明
条件に一致するレコードをSQLを直接実行して全て更新  
updated_atとupdated_onは更新されない

### 使い方
    モデル.update_all(カラム名: 値 [, オプション])

### オプション

オプション  | 説明
------- | -------
:limit | 取得する件数
:order | 並び順

### 例

#### 複数のデータを更新
    User.update_all("name='A'", "category='B')

### 更新メソッドの種類

メソッド           | バリデーションによるバリデーションの有無
----------------- | ---------------
update            | ○
update_all        | ×
update_attributes | ○
update_attribute  | ×

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation.rb#L432)