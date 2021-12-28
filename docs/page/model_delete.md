---
layout: page
---

### 説明

指定した条件に一致するレコードをSQLを直接実行して削除  
関連付けられたモデルは削除しない

### 使い方

    モデル.delete(IDかIDの配列)

### 例

#### 指定した条件に一致するレコードをSQLを直接実行して削除  

    Todo.delete(1)

#### 配列で指定

    Todo.delete([2,3,4])

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/persistence.rb#L474)
