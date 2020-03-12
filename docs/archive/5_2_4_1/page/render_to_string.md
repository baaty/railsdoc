---
layout: archive_page
---
### 説明
表示結果を文字列として取得

### 使い方
    render_to_string(リクエスト)

### 例
#### userテンプレートを取得
    render_to_string partial: "user"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionpack/lib/abstract_controller/rendering.rb#L44)