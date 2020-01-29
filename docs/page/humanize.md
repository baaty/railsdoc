---
layout: page
---
### 説明
最初の単語を大文字にし、スペースやストリップ末尾の_idを削除

### 使い方
    文字列.humanize([capitalize: true, keep_id_suffix: false])

### 例
    'employee_salary'.humanize
    # "Employee salary"

    'author_id'.humanize
    # "Author"

    'author_id'.humanize(capitalize: false)
    # "author"

    '_id'.humanize
    # "Id"

    'author_id'.humanize(keep_id_suffix: true)
    # "Author Id"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activesupport/lib/active_support/core_ext/string/inflections.rb#L236)