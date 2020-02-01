---
layout: page
---
### 説明
クラス名から外部キーの名前を生成
separate_class_name_and_id_with_underscoreがfalseでアンダーバーなし

### 使い方
    文字列.foreign_key([名前とidの間にアンダーバーを入れるか = true])

### 例
#### クラス名から外部キーの名前を生成
    'Message'.foreign_key
    # "message_id"

#### 名前とidの間にアンダーバーを入れない
    'Message'.foreign_key(false)
    # "messageid"

#### 親クラスがある場合
    'Admin::Post'.foreign_key
    # "post_id"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activesupport/lib/active_support/core_ext/string/inflections.rb#L256)