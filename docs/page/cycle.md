---
layout: page
---

### 説明

奇数と偶数で処理を変える

### 使い方

    cycle(値..)

### 補足

- reset_cycleでリセット
- current_cycleで現在の値を取得

### 例

    <ul>
    <% @pages.each do |i| %>
      <li class="<%= cycle("even", "odd") %>">
        <% i %>
      </li%>
    <% end %>
    </ul>
    #=> <ul>
    # <li class="even">page内容1</li>
    # <li class="odd">page内容2</li>
    # <li class="even">page内容3</li>
    # </ul>

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/text_helper.rb#L358)
