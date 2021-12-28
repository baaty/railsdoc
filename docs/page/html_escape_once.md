---
layout: page
---

### 説明

既にエスケープされた文字列はそのままでHTMLタグをエスケープ

### 使い方

    html_escape_once(文字列)

### 例

    html_escape_once('<< Accept & Checkout')
    # "<< Accept & Checkout"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activesupport/lib/active_support/core_ext/string/output_safety.rb#L50)
