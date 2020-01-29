---
layout: page
---
### 説明
あらかじめ指定した値を順番に返す

### 使い方
    current_cycle

### 例
#### 奇数、偶数でclass名を変える
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
    # <ul>
    # <li class="even">page内容1</li>
    # <li class="even">page内容1</li>
    # <li class="odd">page内容2</li>
    # <li class="odd">page内容2</li>
    # <li class="even">page内容3</li>
    # <li class="even">page内容3</li>
    # </ul>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0e50b7bdf4c0f789db37e22dc45c52b082f674b4/actionview/lib/action_view/helpers/text_helper.rb#L359)