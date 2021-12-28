---
layout: page
---

### 説明

文字列内の単語の複数形

### 使い方

    名詞.pluralize([個数, ロケール])

### 例

#### postの複数形

    'post'.pluralize
    # "posts"

#### octopusの複数形

    'octopus'.pluralize
    # "octopi"

#### sheepの複数形

    'sheep'.pluralize
    # "sheep"

#### wordsの複数形

    'words'.pluralize
    # "words"

#### 単語から複数形

    'the blue mailman'.pluralize
    # "the blue mailmen"

#### CamelOctopusの複数形

    'CamelOctopus'.pluralize
    # "CamelOctopi"

#### appleの単数形

    'apple'.pluralize(1)
    # "apple"

#### appleの複数形

    'apple'.pluralize(2)
    # "apples"

#### ロケール指定

    'ley'.pluralize(:es)
    # "leyes"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activesupport/lib/active_support/core_ext/string/inflections.rb#L35)
