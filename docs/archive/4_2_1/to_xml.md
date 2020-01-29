---
layout: page
---
### 説明
モデルオブジェクトをXML形式に変換

### 使い方
    モデル.to_xml

### 例
    User.limit(2).to_xml
    # <?xml version="1.0" encoding="UTF-8"?>
    # <contributors type="array">
    #   <contributor>
    #     <id type="integer">1</id>
    #     <name>Railsの基礎知識</name>
    #   </contributor>
    #   <contributor>
    #     <id type="integer">2</id>
    #     <name>Rubyの基礎知識</name>
    #   </contributor>
    # </contributors>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/6c8cf21584ced73ade45529d11463c74b5a0c58f/activemodel/lib/active_model/errors.rb#L234)