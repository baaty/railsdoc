---
layout: page
---

### 説明

非出力コード内(<% %>)で出力

### 使い方

    concat(文字列)

### 例

    <%
      concat "hello"

      if logged_in
        concat "Logged in!"
      else
        concat link_to('login', action: :login)
      end
    %>

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/text_helper.rb#L58)
