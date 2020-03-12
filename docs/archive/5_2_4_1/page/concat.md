---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/text_helper.rb#L54)