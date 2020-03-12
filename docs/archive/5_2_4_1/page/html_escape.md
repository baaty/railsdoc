---
layout: archive_page
---
### 説明
HTMLタグをエスケープ

### 使い方
    html_escape(文字列)

### 例
#### HTMLタグをエスケープ
    html_escape('is a > 0 & a < 10?')
    # is a &gt; 0 &amp; a &lt; 10?

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activesupport/lib/active_support/core_ext/string/output_safety.rb#L20)