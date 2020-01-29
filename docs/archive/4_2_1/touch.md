---
layout: page
---
### 説明
update_atを現在の時刻でアップデートする。検証やコールバックを実施されない

### 使い方
    モデル.touch([名前])

### 例
    product.touch
    # updates updated_at/on

    product.touch(:designed_at)
    # updates the designed_at attribute and updated_at/on

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/93a6500baa6bbb331bb93ccdc14fdda5769f5ef9/activerecord/lib/active_record/persistence.rb#L453)