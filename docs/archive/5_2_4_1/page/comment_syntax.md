---
layout: archive_page
---
### 説明
Rubyの標準のコメントアウト構文

    <%# コメント %>

    <%#
    複数行のコメントもOK
    %>

### begin
ドキュメンテンーションコメントを記述するときによく使う構文

    <% =begin %>
    <%= コメント %>
    <% =end %>

### <% if false %>
条件文を利用したコメントアウト構文

    <% if false %>
    <%= コメント %>
    <% end %>

### <!--
HTMLの標準のコメントアウト構文

    <!-- コメント -->