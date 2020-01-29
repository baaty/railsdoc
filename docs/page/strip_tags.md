---
layout: page
---
### 説明
HTMLタグを取り除く

### 使い方
    strip_tags(html)

### 例
    strip_tags("Strip <i>these</i> tags!")
    # => Strip these tags!

    strip_tags("<b>Bold</b> no more!  <a href='more.html'>See more here</a>...")
    # => Bold no more!  See more here...

    strip_tags("<div id='top-bar'>Welcome to my website!</div>")
    # => Welcome to my website!

    strip_tags("> A quote from Smith & Wesson")
    # => &gt; A quote from Smith &amp; Wesson

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/sanitize_helper.rb#L103)