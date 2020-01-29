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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/associations/collection_proxy.rb#L689)