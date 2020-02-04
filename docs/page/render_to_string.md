---
layout: page
---
### 説明
表示結果を文字列として取得

### 使い方
    render_to_string(リクエスト)

### 例
#### userテンプレートを取得
    render_to_string partial: "user"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/abstract_controller/rendering.rb#L44)