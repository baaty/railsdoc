---
layout: archive_page
---
### 説明
リンクのみ取り除く

### 使い方
    strip_links(html)

### 例
#### リンクのみ取り除く
    strip_links('<a href="http://www.rubyonrails.org">Ruby on Rails</a>')
    # Ruby on Rails

#### リンクのみ取り除く
    strip_links('Please e-mail me at <a href="mailto:me@email.com">me@email.com</a>.')
    # Please e-mail me at me@email.com.

#### class属性などがある場合
    strip_links('Blog: <a href="http://www.myblog.com/" class="nav" target=\"_blank\">Visit</a>.')
    # Blog: Visit.

#### エスケープされる文字あり
    strip_links('<<a href="https://example.org">malformed & link</a>')
    # &lt;malformed &amp; link

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/sanitize_helper.rb#L121)