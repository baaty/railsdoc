---
layout: page
---

### 説明

最初の単語を大文字にしアンダーバーをスペースへ変換し末尾の\_idを削除

### 使い方

    humanize(単語, capitalize: 最初の単語が大文字か=true, keep_id_suffix: suffix=false)

### オプション

| オプション      | 説明                       | デフォルト値 |
| --------------- | -------------------------- | ------------ |
| :capitalize     | 最初の単語を大文字にするか | true         |
| :keep_id_suffix | 末尾の\_idを残すか         | false        |

### 例

#### 最初の単語を大文字にし、アンダーバーをスペースへ変換

    humanize('employee_salary')
    # "Employee salary"

#### 最初の単語を大文字にし、末尾の\_idを削除

    humanize('author_id')
    # "Author"

#### 最初の単語を大文字しない

    humanize('author_id', capitalize: false)
    # "author"

#### \_idのみ

    humanize('_id')
    # "Id"

#### 末尾の\_idを残す

    humanize('author_id', keep_id_suffix: true)
    # "Author Id"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activesupport/lib/active_support/inflector/methods.rb#L132)
