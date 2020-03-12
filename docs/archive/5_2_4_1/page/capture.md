---
layout: archive_page
---
### 説明
出力結果を変数に格納  
テンプレートの一部を変数に保存することなどが可能

### 使い方
    @var = capture do
      格納する文字列
    end

### 例
#### 出力結果を変数に格納
    <% @time = capture do %>
    現在の時刻は<%= Time.now %>
    <% end %>
    <%= @time %>
    # 現在の時刻は Sat Dec 24 00:00:00 +0900 2011

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/capture_helper.rb#L39)