---
layout: page
---
### 説明
指定された文字列からCDATAセクションを出力

### 使い方
    cdata_section(文字列)

### 例
    cdata_section("<hello world>")
    # <![CDATA[<hello world>]]>

    cdata_section(File.read("hello_world.txt"))
    # <![CDATA[<hello from a text file]]>

    cdata_section("hello]]>world")
    # <![CDATA[hello]]]]><![CDATA[>world]]>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/tag_helper.rb#L292)