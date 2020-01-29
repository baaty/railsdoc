---
layout: page
---
### 説明
複数形の名詞を単数形に変換
「config/initializers/inflections.rb」に定義を追加することによって、不可算名詞を追加できる

### 使い方
    <名詞>.singularize

### 例
#### 「rubies」を単数形に変換
    "rubies".singularize
    # "ruby"

#### 「equipment」を単数形に変換
    "equipment".singularize
    # "equipment"