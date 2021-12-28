---
layout: page
---

### 説明

レイアウトに複数のコンテンツを設定

### 使い方

    content_for(コンテンツ名, コンテンツ=nil, オプション={}, ブロック引数)

### オプション

| オプション | 説明           |
| ---------- | -------------- |
| :flush     | スタックを削除 |

### 例

#### レイアウトに複数のコンテンツを設定

    <% content_for :extend_menu do %>
      [<%= link_to 文字列A, action: "A" %>]
      [<%= link_to 文字列B, action: "B" %>]
    <% end %>

#### スクリプト識別

    <% content_for :script do %>
      <script>alert('You are not authorized to view this page!')</script>
    <% end %>

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/capture_helper.rb#L155)
