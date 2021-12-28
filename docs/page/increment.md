---
layout: page
---

### 説明

特定のレコードをインクリメント

### 使い方

    モデル.increment(レコード, インクリメントする値, touch: タイムスタンプ列=nil)

    # 失敗したら例外発生
    モデル.increment!(レコード, インクリメントする値, touch: タイムスタンプ列=nil)

### 例

    Page.increment(:num, 3)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/persistence.rb#L845)
