---
layout: archive_page
---
### 説明
既にエスケープされた文字列はそのままで、HTMLタグをエスケープ

### 使い方
    html_escape_once(文字列)

### 例
#### HTMLタグをエスケープ
    html_escape_once('&lt;&lt; Accept & Checkout')
    # "&lt;&lt; Accept &amp; Checkout"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activesupport/lib/active_support/core_ext/string/output_safety.rb#L51)