---
layout: page
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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/debug_helper.rb#L26)