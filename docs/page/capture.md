---
layout: page
---

### 説明

出力結果を変数に格納  
テンプレートの一部を変数に保存することなどが可能

### 使い方

    capture(引数..)

### 例

    <% @time = capture do %>
        現在の時刻は<%= Time.now %>
    <% end %>
    <%= @time %>
    #=> 現在の時刻は Sat Dec 24 00:00:00 +0900 2011

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/capture_helper.rb#L43)
