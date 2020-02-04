---
layout: page
---
### 説明
配列またはハッシュをXML形式に変換

### 使い方
    配列.to_xml([オプション])

    ハッシュ.to_xml([オプション])

### オプション

オプション          | 説明
---------------|---------
:root          | ルート要素を指定
:children      | 子要素を指定
:skip_types    |
:indent        | インデントを指定
:builder       | XMLビルダを指定
:skip_instruct | ヘッダのタグを非表示

### 例
#### 配列をXML形式
    [{ foo: 1, bar: 2}, { baz: 3}].to_xml
    # <?xml version="1.0" encoding="UTF-8"?>
    # <objects type="array">
    #   <object>
    #     <bar type="integer">2</bar>
    #     <foo type="integer">1</foo>
    #   </object>
    #   <object>
    #     <baz type="integer">3</baz>
    #   </object>
    # </objects>

#### ハッシュをXML形式
    { foo: 1, bar: 2 }.to_xml
    # =>
    # <?xml version="1.0" encoding="UTF-8"?>
    # <hash>
    #   <foo type="integer">1</foo>
    #   <bar type="integer">2</bar>
    # </hash>