---
layout: page
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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/text_helper.rb#L354)