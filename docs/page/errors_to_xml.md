---
layout: page
---

### 説明

Errorsのハッシュのxml形式を取得

### 使い方

    モデル.errors.to_xml(オプション={})

### 例

    person.errors.add(:name, :blank, message: "can't be blank")
    person.errors.add(:name, :not_specified, message: "must be specified")
    person.errors.to_xml
    #=>
    #  <?xml version=\"1.0\" encoding=\"UTF-8\"?>
    #  <errors>
    #    <error>name can't be blank</error>
    #    <error>name must be specified</error>
    #  </errors>

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activemodel/lib/active_model/errors.rb#L241)
