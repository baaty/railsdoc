---
layout: page
---
### 説明
デバッグなどで変数の中身を確認したいときなどに使用

### 使い方
    debug(オブジェクト)

### 例
    <% @categories = Category.all %>
    <%= debug(@categories) %>
    # [#<Category id: 1, name: "Railsの基礎知識">, #<Category id: 2, name: "Rubyの基礎知識">]

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/c782641002b7df1ecd693a6c5c439f3a4c036351/actionview/lib/action_view/helpers/debug_helper.rb#L25)