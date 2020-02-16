---
layout: page
---
### 説明
複数レコードを一括登録  
直接SQLを実行するのでバリデーションやコールバックはスキップ  
insert_all!はエラーの時に例外が発生

### 使い方
    insert_all(属性 [, オプション])

### オプション

オプション      | 説明
-----------|-------------------------------------
:returning | 戻り値の属性を指定(PostgreSQLのみ)
:unique_by | 重複でスキップするカラムを指定(PostgreSQLとSQLiteのみ)

### 例
#### 複数レコードを一括登録
    Book.insert_all([
      { id: 1, title: "Rework", author: "David" },
      { id: 1, title: "Eloquent Ruby", author: "Russ" }
    ])

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/persistence.rb#L123)