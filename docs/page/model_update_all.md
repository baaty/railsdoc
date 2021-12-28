---
layout: page
---

### 説明

条件に一致するレコードをSQLを直接実行して全て更新  
updated_atとupdated_onは更新されない

### 使い方

    モデル.update_all(SQL文のSET部分、配列、またはハッシュ)

### オプション

| オプション | 説明         |
| ---------- | ------------ |
| :limit     | 取得する件数 |
| :order     | 並び順       |

### 例

#### 与えられた属性を持つすべてのデータを更新

    Customer.update_all wants_email: true

#### 条件を絞り込んで更新

    Book.where('title LIKE ?', '%Rails%').update_all(author: 'David')

#### 更新するデータ数を固定

    Book.where('title LIKE ?', '%Rails%').order(:created_at).limit(5).update_all(author: 'David')

#### 全てのデータを更新して指定したカラムに値を設定

    Invoice.update_all('number = id')

### 更新メソッドの種類

| メソッド          | バリデーションによるバリデーションの有無 |
| ----------------- | ---------------------------------------- |
| update            | ○                                        |
| update_all        | ×                                        |
| update_attribute  | ×                                        |

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation.rb#L464)
