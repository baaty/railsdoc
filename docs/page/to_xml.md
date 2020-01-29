---
layout: page
---
### 説明
配列またはハッシュをXML形式に変換

### 使い方
    配列.to_xml

    ハッシュ.to_xml

### 例
    { foo: 1, bar: 2 }.to_xml
    # =>
    # <?xml version="1.0" encoding="UTF-8"?>
    # <hash>
    #   <foo type="integer">1</foo>
    #   <bar type="integer">2</bar>
    # </hash>