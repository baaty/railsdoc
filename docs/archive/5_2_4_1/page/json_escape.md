---
layout: archive_page
---
### 説明
JSONエスケープ

### 使い方
    json_escape(文字列)

### 例
#### JSONエスケープ
    json_escape(json)
    # "{\"name\":\"\\u003C/script\\u003E\\u003Cscript\\u003Ealert('PWNED!!!')\\u003C/script\\u003E\"}"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activesupport/lib/active_support/core_ext/string/output_safety.rb#L113)