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

| メソッド          | バリデーションによるバリデーションの有無 |
| ----------------- | ---------------------------------------- |
| update            | ○                                        |
| update_all        | ×                                        |
| update_attribute  | ×                                        |

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/persistence.rb#L754)
