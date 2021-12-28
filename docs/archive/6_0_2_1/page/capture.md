---
layout: page
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
* [GitHub](https://github.com/rails/rails/blob/479c7cacd5db58ab7200bc1de58c829a1a643278/actionview/lib/action_view/helpers/capture_helper.rb#L36)