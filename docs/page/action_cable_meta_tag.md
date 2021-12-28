---
layout: page
---

### 説明

action-cable-urlのメタタグを生成

### 使い方

    action_cable_meta_tag()

### 例

    <head>
        <%= action_cable_meta_tag %>
        <%= javascript_include_tag 'application', 'data-turbo-track' => 'reload' %>
    </head>

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actioncable/lib/action_cable/helpers/action_cable_helper.rb#L34)
