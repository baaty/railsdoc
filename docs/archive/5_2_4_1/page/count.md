---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/calculations.rb#L41)