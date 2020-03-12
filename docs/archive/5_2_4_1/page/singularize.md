---
layout: archive_page
---
### 説明
複数形の名詞を単数形に変換  
「config/initializers/inflections.rb」に定義を追加することによって、不可算名詞の追加が可能

### 使い方
    singularize(文字列 [, ロケーション])

### 例
#### 複数形の名詞を単数形に変換
    singularize('posts')
    # "post"

#### 不可算名詞
    singularize('octopi')
    # "octopus"

#### 不可算名詞
    singularize('sheep')
    # "sheep"

#### キャメルケース
    singularize('CamelOctopi')
    # "CamelOctopus"

#### ロケーション指定
    singularize('leyes', :js)
    # "ley"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activesupport/lib/active_support/inflector/methods.rb#L49)