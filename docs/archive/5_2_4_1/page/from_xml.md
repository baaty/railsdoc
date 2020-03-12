---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activesupport/lib/active_support/core_ext/hash/conversions.rb#L129)