---
layout: archive_page
---
### 説明
奇数と偶数で処理を変える

### 使い方
    cycle(値 [, ..])

### 補足
* reset_cycleでリセット
* current_cycleで現在の値を取得

### 例
#### 奇数、偶数でclass名を変える
    <ul>
    <% @pages.each do |i| %>
      <li class="<%= cycle("even", "odd") %>">
        <% i %>
      </li%>
    <% end %>
    </ul>
    # <ul>
    # <li class="even">page内容1</li>
    # <li class="odd">page内容2</li>
    # <li class="even">page内容3</li>
    # </ul>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/text_helper.rb#L354)