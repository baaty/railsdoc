---
layout: page
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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activesupport/lib/active_support/core_ext/string/output_safety.rb#L51)