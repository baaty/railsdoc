---
layout: page
---

### 説明

指定した文字列からCDATAセクションを出力

### 使い方

    cdata_section(文字列)

### 例

#### 指定した文字列からCDATAセクションを出力

    cdata_section("<hello world>")
    #=> <![CDATA[<hello world>]]>

#### ファイルから読み込む

    cdata_section(File.read("hello_world.txt"))
    #=> <![CDATA[<hello from a text file]]>

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/tag_helper.rb#L375)
