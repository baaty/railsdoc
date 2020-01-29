---
layout: page
---
### 説明
フラグメントキャッシュを有効にするか

### 使い方
    cache_if(条件式 [, キー名, オプション])

### 例
    <% cache_if admin?, project do %>
      <b>All the topics on this project</b>
      <%= render project.topics %>
    <% end %>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/cache_helper.rb#L183)