---
layout: page
---
### 説明
モデルのレコード数を取得

### 使い方
    モデル.count(カラム名)

### 例
#### テーブルの行数を計算
    User.count

#### カラム指定
    Person.count(:age)

#### groupで集計してから件数取得
    Person.group(:city).count
    # {Rome: 5, Paris: 3 }

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/calculations.rb#L41)