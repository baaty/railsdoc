---
layout: page
---
### 説明
XML形式のデータをハッシュに変換

### 使い方
    Hash.from_xml(XMLデータ)

### 例
#### XML形式のデータをハッシュに変換
    Hash.from_xml("<langs><lang>Japanese</lang><lang>English</lang></langs>")
    # {"langs"=>{"lang"=>["Japanese", "English"]}}

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activesupport/lib/active_support/core_ext/hash/conversions.rb#L129)