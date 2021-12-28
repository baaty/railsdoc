---
layout: page
---

### 説明

HTMLのタイムタグを生成

### 使い方

    time_tag(DateかTime, 引数.., ブロック引数)

### 例

#### タイムタグを生成

    time_tag Date.today
    #=> <time datetime="2010-11-04">November 04, 2010</time>

#### ブロック

    <%= time_tag Time.now do %>
        <span>Right now</span>
    <% end %>
    #=> <time datetime="2010-11-04T17:55:45+01:00"><span>Right now</span></time>

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/date_helper.rb#L686)
