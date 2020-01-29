---
layout: page
---
### 説明
HTMLタグをエスケープ

### 使い方
    html_escape(文字列)

### 例
    html_escape('is a > 0 & a < 10?')
    # is a &gt; 0 &amp; a &lt; 10?

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activesupport/lib/active_support/core_ext/string/output_safety.rb#L20)