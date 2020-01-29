---
layout: page
---
### 説明
複数形の名詞を単数形に変換
「config/initializers/inflections.rb」に定義を追加することによって、不可算名詞を追加できる

### 使い方
    名詞.singularize

### 例
    'posts'.singularize
    # "post"

    'octopi'.singularize
    # "octopus"

    'sheep'.singularize
    # "sheep"

    'word'.singularize
    # "word"

    'the blue mailmen'.singularize
    # "the blue mailman"

    'CamelOctopi'.singularize
    # "CamelOctopus"

    'leyes'.singularize(:es)
    # "ley"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activesupport/lib/active_support/core_ext/string/inflections.rb#L56)