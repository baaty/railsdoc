---
layout: page
---

### 説明

XML形式のデータをハッシュに変換

### 使い方

    Hash.from_xml(XMLデータ, 禁止された型=nil)

### 例

    Hash.from_xml("<langs><lang>Japanese</lang><lang>English</lang></langs>")
    # {"langs"=>{"lang"=>["Japanese", "English"]}}

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activesupport/lib/active_support/core_ext/hash/conversions.rb#L129)
