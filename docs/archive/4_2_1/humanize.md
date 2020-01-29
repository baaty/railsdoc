---
layout: page
---
### 説明
最初の単語を大文字にし、スペースやストリップ末尾の_idを削除

### 使い方
    文字列.humanize()

### 例
    'employee_salary'.humanize
    # "Employee salary"

    'author_id'.humanize
    # "Author"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/861b70e92f4a1fc0e465ffcf2ee62680519c8f6f/activesupport/lib/active_support/inflector/methods.rb#L124)