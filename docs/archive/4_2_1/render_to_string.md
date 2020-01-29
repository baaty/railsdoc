---
layout: page
---
### 説明
表示結果を文字列として取得

### 使い方
    render_to_string :partial => "テンプレート名"

### 例
#### userテンプレートを取得
    render_to_string :partial => "user"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f6d9b689977c1dca1ed7f149f704d1b4344cd691/actionpack/lib/abstract_controller/rendering.rb#L41)