---
layout: page
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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/sanitize_helper.rb#L120)