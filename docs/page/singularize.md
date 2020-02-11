---
layout: page
---
### 説明
複数形の名詞を単数形に変換  
「config/initializers/inflections.rb」に定義を追加することによって、不可算名詞の追加が可能

### 使い方
    文字列.singularize([ロケーション])

### 例
#### 複数形の名詞を単数形に変換
    'posts'.singularize
    # "post"

#### 不可算名詞
    'octopi'.singularize
    # "octopus"

#### 不可算名詞
    'sheep'.singularize
    # "sheep"

#### 文字列
    'the blue mailmen'.singularize
    # "the blue mailman"

#### キャメルケース
    'CamelOctopi'.singularize
    # "CamelOctopus"

#### ロケーション指定
    'leyes'.singularize(:js)
    # "ley"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activesupport/lib/active_support/core_ext/string/inflections.rb#L56)