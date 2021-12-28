---
layout: page
---

### 説明

コントローラで処理された内容を埋め込む先を指定

### 使い方

    <%= yield %>

### 例

#### コントローラで処理された内容を埋め込む先を指定

    <body>
        <%= yield %>
    </body>

#### headerの時にjavaScriptのタグを表示

    # app/layouts/application.html.erb
    <body>
        <%= yield :header %>
    </body>

    # app/views/pages/show.thml.erb
    <% content_for :header do %>
        <%= javascript_include_tag "page.js" %>
    <% end %>
