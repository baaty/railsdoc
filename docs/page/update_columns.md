---
layout: page
---

### 説明

SQL文を発行してデータベースの属性を直接更新

### 使い方

    モデル.update_columns(属性)

### 例

    user.update_columns(last_request_at: Time.current)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/persistence.rb#L806)
