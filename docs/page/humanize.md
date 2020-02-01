---
layout: page
---
### 説明
最初の単語を大文字にし、アンダーバーをスペースへ変換し、末尾の_idを削除

### 使い方
    文字列.humanize([オプション])

### オプション

オプション           | 説明                 | デフォルト値
----------------|--------------------|-------
:capitalize     | 最初の単語を大文字にするか | true
:keep_id_suffix | 末尾の_idを残すか        | false

### 例
#### 最初の単語を大文字にし、アンダーバーをスペースへ変換
    'employee_salary'.humanize
    # "Employee salary"

#### 最初の単語を大文字にし、末尾の_idを削除
    'author_id'.humanize
    # "Author"

#### 最初の単語を大文字しない
    'author_id'.humanize(capitalize: false)
    # "author"

#### _idのみ
    '_id'.humanize
    # "Id"

#### 末尾の_idを残す
    'author_id'.humanize(keep_id_suffix: true)
    # "Author Id"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activesupport/lib/active_support/core_ext/string/inflections.rb#L236)