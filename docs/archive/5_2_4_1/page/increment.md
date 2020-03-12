---
layout: archive_page
---
### 説明
特定のレコードをインクリメント

### 使い方
    モデル.increment(レコード, インクリメントする値)

### 例
#### Pageテーブルのnumレコードを3ずつインクリメント
    Page.increment(:num, 3)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/persistence.rb#L504)