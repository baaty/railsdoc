---
layout: page
---

### 説明

あらかじめ指定した値を順番に取得

### 使い方

    current_cycle(名前='default')

### 例

    <ul>
    <% @pages.each do |i| %>
      <li class="<%= cycle("even", "odd") %>">
        <% i %>
      </li%>
      <li class="<%= current_cycle %>">
        <% i %>
      </li%>
    <% end %>
    </ul>
    #=> <ul>
    # <li class="even">page内容1</li>
    # <li class="even">page内容1</li>
    # <li class="odd">page内容2</li>
    # <li class="odd">page内容2</li>
    # <li class="even">page内容3</li>
    # <li class="even">page内容3</li>
    # </ul>

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/text_helper.rb#L382)
