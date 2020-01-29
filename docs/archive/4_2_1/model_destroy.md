---
layout: page
---
### 使い方
    モデル.destroy([引数 or 配列])

### 例
#### ロードしたオブジェクトを削除
    entry = Entry.find(:first)<br />entry.destroy

#### モデルオブジェクトのロードと削除を一度に行う
    Entry.destroy([1, 2])

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/39c1d2e1840674f2a58dc1ba610fd64a37e950fd/activerecord/lib/active_record/associations/collection_proxy.rb#L659)