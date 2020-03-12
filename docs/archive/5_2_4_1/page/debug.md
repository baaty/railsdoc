---
layout: archive_page
---
### 説明
デバッグなどで変数の中身を確認したいときなどに使用

### 使い方
    debug(オブジェクト)

### 例
#### デバッグ表示
    debug(@categories)
    # [#<Category id: 1, name: "Railsの基礎知識">, #<Category id: 2, name: "Rubyの基礎知識">]

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/debug_helper.rb#L26)