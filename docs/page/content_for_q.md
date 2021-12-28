---
layout: page
---

### 説明

content_forを使用してコンテンツがまだキャプチャされていないかどうかをチェック

### 使い方

    content_for?(名前)

### 例

    <%# This is the layout %>
    <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
    <head>
      <title>My Website</title>
      <%= yield :script %>
    </head>
    <body class="<%= content_for?(:right_col) ? 'two-column' : 'one-column' %>">
      <%= yield %>
      <%= yield :right_col %>
    </body>
    </html>

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/capture_helper.rb#L195)
