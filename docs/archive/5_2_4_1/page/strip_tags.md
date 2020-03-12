---
layout: archive_page
---
### 説明
HTMLタグを取り除く

### 使い方
    strip_tags(html)

### 例
#### HTMLタグを取り除く
    strip_tags("Strip <i>these</i> tags!")
    # => Strip these tags!

#### 複数箇所でタグあり
    strip_tags("<b>Bold</b> no more!  <a href='more.html'>See more here</a>...")
    # => Bold no more!  See more here...

#### エスケープされる文字あり
    strip_tags("> A quote from Smith & Wesson")
    # => &gt; A quote from Smith &amp; Wesson

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/sanitize_helper.rb#L104)