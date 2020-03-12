---
layout: archive_page
---
### 説明
フラグメントキャッシュが有効かチェック

### 使い方
    cache_if(条件式 [, キー名, オプション])

### 例
    <% cache_if admin?, project do %>
      <b>All the topics on this project</b>
      <%= render project.topics %>
    <% end %>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/cache_helper.rb#L183)