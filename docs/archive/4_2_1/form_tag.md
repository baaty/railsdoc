---
layout: page
---
### 説明
特定のモデルに特化したフォームを生成

### 使い方
    form_tag(リンク先 [オプション]) do
    end

### オプション

オプション               | 説明
------------------- | -------------------------
:multipart          | マルチパートを指定
:method             | HTTPメソッドを指定
:authenticity_token | authenticity_tokenを比較して返す
:remote             | Ajaxでリンクを処理
:id                 | idを指定
:class              | classを指定

### 例
#### 基本形(オプションなし)
    <%= form_tag('/users') do %>
    <% end %>
    # <form action="users" method="put">
    # </form>

#### putメソッド指定
    <%= form_tag('/users', :method => :put) do %>
    <% end %>
    # <form action="users" method="post">
    # </form>

#### multipart指定
    <%= form_tag('/users', :multipart => true) do %>
    <% end %>
    # <form action="users" method="post" enctype="multipart/form-data">
    # </form>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/dd7af2c413a06ea44e50abf0df205314ba1bfc98/actionview/lib/action_view/helpers/form_tag_helper.rb#L67)