---
layout: page
---
### 説明
レイアウトに複数のコンテンツを設定

### 使い方
    content_for コンテンツ名 do
    &nbsp;&nbsp;コンテンツ
    end

### 例
レイアウトに複数のコンテンツを設定

    layouts/xxx
    ・・・
    <%=  yield :extend_menu %>
    ・・・
    <%= yield %>
    ・・・

    views/xxx
    <% content_for :extend_menu do %>
      [<%= link_to 文字列A, action => "A" %>]
      [<%= link_to 文字列B, action => "B" %>]
    <% end %>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/479c7cacd5db58ab7200bc1de58c829a1a643278/actionview/lib/action_view/helpers/capture_helper.rb#L148)