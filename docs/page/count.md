---
layout: page
---

### 説明

モデルのレコード数を取得

### 使い方

    モデルのコレクション.count(カラム名=nil)

### 例

#### テーブルの行数を計算

    User.count

#### カラム指定

    Person.count(:age)

#### groupで集計してから件数取得

    Person.group(:city).count

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/calculations.rb#L43)
