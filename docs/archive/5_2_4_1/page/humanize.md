---
layout: archive_page
---
### 説明
最初の単語を大文字にし、アンダーバーをスペースへ変換し、末尾の_idを削除

### 使い方
    humanize(文字列 [, オプション])

### オプション

オプション           | 説明                 | デフォルト値
----------------|--------------------|-------
:capitalize     | 最初の単語を大文字にするか | true
:keep_id_suffix | 末尾の_idを残すか        | false

### 例
#### 最初の単語を大文字にし、アンダーバーをスペースへ変換
    humanize('employee_salary')
    # "Employee salary"

#### 最初の単語を大文字にし、末尾の_idを削除
    humanize('author_id')
    # "Author"

#### 最初の単語を大文字しない
    humanize('author_id', capitalize: false)
    # "author"

#### _idのみ
    humanize('_id')
    # "Id"

#### 末尾の_idを残す
    humanize('author_id', keep_id_suffix: true)
    # "Author Id"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activesupport/lib/active_support/inflector/methods.rb#L129)