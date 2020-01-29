---
layout: page
---
### 説明
クラス名から外部キーの名前を生成
separate_class_name_and_id_with_underscoreがfalseでアンダーバーなし

### 使い方
    文字列.foreign_key([separate_class_name_and_id_with_underscore = true])

### 例
    'Message'.foreign_key
    # "message_id"

    'Message'.foreign_key(false)
    # "messageid"

    'Admin::Post'.foreign_key
    # "post_id"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activesupport/lib/active_support/core_ext/string/inflections.rb#L256)