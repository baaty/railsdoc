---
layout: page
---

### 説明

javascriptの改行やシングルおよびダブルクォートをエスケープ

### 使い方

    escape_javascript(javascript)

    j(javascript)

### 例

#### javascriptの改行やシングルおよびダブルクォートをエスケープ

    $('some_element').replaceWith('<%= escape_javascript render 'some/element_template' %>');

#### 短縮系

    $('some_element').replaceWith('<%= j render 'some/element_template' %>');

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/javascript_helper.rb#L27)
