---
layout: page
---
### 説明
特定のレコードをインクリメント

### 使い方
    モデル.increment(レコード, インクリメントする値)

### 例
#### Pageテーブルのnumレコードを3ずつインクリメント
    Page.increment(:num, 3)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/persistence.rb#L692)