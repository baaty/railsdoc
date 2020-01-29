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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/text_helper.rb#L54)