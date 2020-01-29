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
* [GitHub](https://github.com/rails/rails/blob/6b0e834a194d112585f41deba0a40780d68e38c6/activemodel/lib/active_model/serializers/xml.rb#L232)