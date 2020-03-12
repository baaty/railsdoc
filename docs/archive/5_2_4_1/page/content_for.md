---
layout: archive_page
---
### 説明
レイアウトに複数のコンテンツを設定

### 使い方
    content_for コンテンツ名 [, コンテンツ, オプション] do
      コンテンツ
    end

### オプション

オプション | 説明
-------- | ---------
:flush   | スタックを削除

### 例
#### レイアウトに複数のコンテンツを設定
    <% content_for :extend_menu do %>
      [<%= link_to 文字列A, action: "A" %>]
      [<%= link_to 文字列B, action: "B" %>]
    <% end %>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/capture_helper.rb#L151)