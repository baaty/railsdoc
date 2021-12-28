---
layout: page
---
### 説明
既存の並び順を指定した条件に置き換える

### 使い方
    モデル.reorder(ソート式)

### 並び順

並び順 | 説明
------|--------------
ASC   | 小さい方から大きい方に並ぶ(昇順)
DESC  | 大きい方から小さい方に並ぶ(降順)

### 例
#### 既存の並び順を指定した条件に置き換える
    User.order('email DESC').reorder('id ASC')
    # generated SQL has 'ORDER BY id ASC'

#### reorderより後の並び順は追加
    User.order('email DESC').reorder('id ASC').order('name ASC')

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/query_methods.rb#L379)