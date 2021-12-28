---
layout: page
---

### 説明

複数レコードを一括登録  
直接SQLを実行するのでバリデーションやコールバックはスキップ

### 使い方

    モデル.insert_all(属性, returning: nil, unique_by: nil, record_timestamps: nil)

    # 失敗したら例外発生
    モデル.insert_all!(属性, returning: nil, unique_by: nil, record_timestamps: nil)

### オプション

| オプション         | 説明                                                   |
| ------------------ | ------------------------------------------------------ |
| :returning         | 戻り値の属性を指定(PostgreSQLのみ)                     |
| :unique_by         | 重複でスキップするカラムを指定(PostgreSQLとSQLiteのみ) |
| :record_timestamps | タイムスタンプの自動設定を強制                         |

### 例

    Book.insert_all([
      { id: 1, title: "Rework", author: "David" },
      { id: 1, title: "Eloquent Ruby", author: "Russ" }
    ])

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/persistence.rb#L145)
