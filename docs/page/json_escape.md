---
layout: page
---

### 説明

JSONエスケープ

### 使い方

    json_escape(文字列)

### 例

    json_escape(json)
    # "{\"name\":\"\\u003C/script\\u003E\\u003Cscript\\u003Ealert('PWNED!!!')\\u003C/script\\u003E\"}"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activesupport/lib/active_support/core_ext/string/output_safety.rb#L112)
