---
layout: page
---

### 説明

分割してレコードを取得して処理  
デフォルトで1000件ずつ処理

### 使い方

    モデル.in_batches([オプション]) do |i|
      処理内容
    end

### オプション

| オプション       | 説明               | デフォルト値 |
| ---------------- | ------------------ | ------------ |
| :of              | 同時処理数         | 1000         |
| :load            | ロードするか       | false        |
| :start           | 処理開始位置       |              |
| :finish          | 終了するときのキー |              |
| :error_on_ignore | 例外を発生させる   |              |
| :order           | 主キーの順序を指定 | :asc         |

### 例

#### 分割してレコードを取得して処理

    Person.where("age > 21").in_batches do |relation|
      relation.delete_all
      sleep(10) # Throttle the delete queries
    end

#### 分割して取得して削除

    Person.in_batches.delete_all

#### 分割して取得して更新

    Person.in_batches.update_all(awesome: true)

### 補足

- find_in_batchesとの違いはActiveRecord::Relationで値を返す

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/batches.rb#L204)
