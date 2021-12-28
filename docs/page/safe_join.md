---
layout: page
---

### 説明

HTMLセーフなJOIN

### 使い方

    safe_join(配列, sep = $,)

### 例

    safe_join([raw("<p>foo</p>"), "<p>bar</p>"], "<br />")
    #=> "<p>foo</p><br /&gt;<p&gt;bar</p&gt;"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/output_safety_helper.rb#L33)
