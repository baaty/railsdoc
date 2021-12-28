---
layout: page
---

### 説明

コンテンツを含んだJavaScriptタグを生成

### 使い方

    javascript_tag(コンテンツ=nil, HTMLオプション=nil, ブロック引数)

### 例

#### JavaScriptタグを生成

    javascript_tag "alert('All is good')"

#### HTMLオプション

    javascript_tag "alert('All is good')", type: 'application/javascript'

#### ブロック

    <%= javascript_tag type: 'application/javascript' do -%>
      alert('All is good')
    <% end -%>

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/javascript_helper.rb#L74)
