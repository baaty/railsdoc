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
* [GitHub](https://github.com/rails/rails/blob/93a6500baa6bbb331bb93ccdc14fdda5769f5ef9/activerecord/lib/active_record/persistence.rb#L310)