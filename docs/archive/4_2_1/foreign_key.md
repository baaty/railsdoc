---
layout: page
---
### 説明
クラス名から外部キーの名前を作成
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
* [GitHub](https://github.com/rails/rails/blob/861b70e92f4a1fc0e465ffcf2ee62680519c8f6f/activesupport/lib/active_support/inflector/methods.rb#L227)