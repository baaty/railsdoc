---
layout: page
---

### 説明

HTMLタグを取り除く

### 使い方

    strip_tags(html)

### 例

#### HTMLタグを取り除く

    strip_tags("Strip <i>these</i> tags!")
    # Strip these tags!

#### 複数箇所でタグあり

    strip_tags("<b>Bold</b> no more!  <a href='more.html'>See more here</a>...")
    # Bold no more!  See more here...

#### エスケープされる文字あり

    strip_tags("> A quote from Smith & Wesson")
    # > A quote from Smith & Wesson

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/sanitize_helper.rb#L103)
