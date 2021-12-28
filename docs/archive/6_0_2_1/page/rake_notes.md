---
layout: page
---
### 説明
ソースコードに記入された「FIXME, OPTIMIZE, TODO」を検索して表示

### 使い方
    $ rake notes

### 例
#### ソースコードにやり残しを記述
    def test
    # TODO: やり残し
    end

    $ rake notes
      * [  3] [TODO] やり残し