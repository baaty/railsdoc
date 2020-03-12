---
layout: archive_page
---
### 説明
あらかじめ指定した値を順番に取得

### 使い方
    current_cycle(名前)

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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/text_helper.rb#L378)